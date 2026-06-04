
  ![on-push](../../actions/workflows/on-push.yaml/badge.svg)
  ![on-pull-request](../../actions/workflows/on-pull-request.yaml/badge.svg)
  ![on-schedule](../../actions/workflows/on-schedule.yaml/badge.svg)

  # UAlbertaVISUAL's Website

  Visit **[ualbertavisual.ca](https://ualbertavisual.ca)** 🚀

  _Built with [Lab Website Template](https://greene-lab.gitbook.io/lab-website-template-docs)_

  ## Content update guide

  This site is a Jekyll website. Most content updates are made by adding or editing Markdown and YAML files in a few specific folders.

  ### Quick reference

  | What you want to add | File(s) to edit | Folder |
  | --- | --- | --- |
  | Team member | `_members/<slug>.md` | `/_members/` |
  | Team member photo | image file referenced by `image:` | `/images/` |
  | Google Scholar publications source | `_data/google-scholar.yaml` | `/_data/` |
  | Project detail page | `index.md` inside a project folder | `/projects/<slug>/` |
  | Project listing / featured banner card | `_data/projects.yaml` | `/_data/` |
  | Project images | image files referenced by project page and project card | `/images/project_images/<slug>/` |
  | Blog post | `YYYY-MM-DD-post-title.md` | `/_posts/` |
  | Blog post image | image file referenced by `image:` | `/images/blog/<post-slug>/` |

  > Do **not** manually edit `/_data/citations.yaml`. It is generated automatically from the Google Scholar source list.

  ---

  ## 1) Add a new team member

  Team members are stored as Markdown files in `/_members/`. Each file becomes that member's profile page automatically.

  ### Step 1: Choose a filename

  Create a new file in:

  ```text
  /_members/<slug>.md
  ```

  Use a short lowercase slug for the filename, for example:

  ```text
  /_members/jane-doe.md
  ```

  That filename becomes the member page slug used elsewhere in the site.

  ### Step 2: Add the member photo

  Add the person's image somewhere under `/images/`.

  Example:

  ```text
  /images/Jane_Doe/jane-doe.jpg
  ```

  ### Step 3: Add the member Markdown file

  Use this format:

  ```md
  ---
  name: Jane Doe
  image: images/Jane_Doe/jane-doe.jpg
  role: phd
  affiliation: University of Alberta
  description: PhD Candidate
  aliases:
    - Jane Doe
  links:
    email: janedoe@ualberta.ca
    google-scholar: ScholarUserIdHere
    github: jane-doe
    linkedin: jane-doe
  ---

  #### Joined: September 2026
  #### Co-supervisor: Prof. Example Name

  Write the member bio here in Markdown.
  ```

  ### Required fields

  - `name`: display name on the website
  - `image`: path to the portrait image under `/images/`
  - `role`: controls where the member appears on `/team/`

  ### Common optional fields

  - `affiliation`
  - `description`
  - `aliases`
  - `links` such as `email`, `google-scholar`, `github`, `linkedin`, `home-page`

  ### Role values currently shown on the Team page

  The Team page currently renders these roles:

  - `principal-investigator`
  - `postdoc`
  - `phd`
  - `ms`
  - `undergrad`

  If you use a different role value, the member file may exist, but it will not show on `/team/` unless the team page is updated too.

  ### Step 4: Commit and verify

  Once the file and image are added, the member will automatically appear on the Team page in the section matching their `role`.

  ---

  ## 2) Add a new Google Scholar source to the research papers list

  The Research page is built from generated citation data. To add papers from a new Google Scholar profile, update the Google Scholar source list, not the generated citations file.

  ### Step 1: Get the Google Scholar user ID

  From a profile URL like:

  ```text
  https://scholar.google.com/citations?user=abcd1234EFGH
  ```

  the user ID is:

  ```text
  abcd1234EFGH
  ```

  ### Step 2: Make sure the member exists

  If the scholar profile belongs to a lab member, first create or confirm the member file exists in:

  ```text
  /_members/<member-slug>.md
  ```

  If you want the Google Scholar icon on the member page, also include the same Scholar ID in that member file:

  ```yaml
  links:
    google-scholar: abcd1234EFGH
  ```

  ### Step 3: Add the scholar source entry

  Edit:

  ```text
  /_data/google-scholar.yaml
  ```

  Add a new item in this format:

  ```yaml
  - gsid: abcd1234EFGH
    research_page: true
    member: jane-doe
  ```

  ### Field meanings

  - `gsid`: Google Scholar user ID
  - `research_page: true`: includes that scholar's papers on the main `/research/` page
  - `member`: must match the member file slug, such as `jane-doe`

  ### Step 4: Let the citations regenerate

  The repository has a workflow that rebuilds `/_data/citations.yaml` from the entries in `/_data/google-scholar.yaml`.

  So the normal process is:

  1. Add the scholar source to `/_data/google-scholar.yaml`
  2. Push the change
  3. Let the citation update workflow regenerate `/_data/citations.yaml`
  4. Confirm the new papers appear on `/research/`

  ### Important notes

  - Do **not** manually maintain `/_data/citations.yaml`
  - If `research_page` is not set to `true`, the papers will not appear in the main research list
  - The `member` slug should match the member filename slug

  ---

  ## 3) Add a new project page

  Projects have two parts:

  1. a full project page in `/projects/<slug>/index.md`
  2. a listing entry in `/_data/projects.yaml`

  ### Step 1: Create the project folder

  Create a new folder:

  ```text
  /projects/<slug>/
  ```

  Example:

  ```text
  /projects/2026_jane_example_project/
  ```

  ### Step 2: Copy the project template

  Use this file as the starting point:

  ```text
  /projects/sample-project/index.md
  ```

  Copy it to:

  ```text
  /projects/<slug>/index.md
  ```

  ### Step 3: Add project images

  Create a matching image folder, for example:

  ```text
  /images/project_images/<slug>/
  ```

  Put the project artwork there and reference it from the page.

  ### Step 4: Fill out the project page

  The page file should stay as Markdown with front matter at the top. A typical structure is:

  ```md
  ---
  title: My Project Title
  description: Short summary of the project page.
  ---

  # My Project Title

  {% include section.html %}

  {% include figure.html
    image="images/project_images/<slug>/project-image.png"
    caption="Project overview image"
    width="100%"
  %}

  ## Abstract
  ...

  ## Team
  ...

  ## Links
  ...

  ## Methods
  ...

  ## Results
  ...

  ## Citation
  ...
  ```

  ### Step 5: Add the project card to the Projects page

  Edit:

  ```text
  /_data/projects.yaml
  ```

  Add a new entry in this format:

  ```yaml
  - title: My Project Title
    subtitle: Conference / Journal / Year
    image: images/project_images/<slug>/project-image.png
    link: projects/<slug>
    description: One-sentence summary of the project.
    tags:
      - medical imaging
      - segmentation
  ```

  ### Optional fields

  - `group: featured` — makes it appear in the **Featured** section on `/projects/`
  - `repo: owner/repository-name` — shows a repository badge if needed

  ### How to make it show as a banner / featured item on the main Projects page

  In `/_data/projects.yaml`, add:

  ```yaml
  group: featured
  ```

  Example:

  ```yaml
  - title: My Project Title
    subtitle: Conference / Journal / Year
    group: featured
    image: images/project_images/<slug>/project-image.png
    link: projects/<slug>
    description: One-sentence summary of the project.
    tags:
      - medical imaging
  ```

  If `group: featured` is omitted, the project goes into the **More** section instead of the top featured area.

  ---

  ## 4) Add a blog post

  Blog posts are regular Jekyll posts stored in `/_posts/`.

  ### Step 1: Choose the filename

  Create the post in this format:

  ```text
  /_posts/YYYY-MM-DD-your-post-title.md
  ```

  Example:

  ```text
  /_posts/2026-06-04-my-new-blog-post.md
  ```

  ### Step 2: Add the post image

  Add any blog image under a folder such as:

  ```text
  /images/blog/my-new-blog-post/
  ```

  Example image path:

  ```text
  images/blog/my-new-blog-post/cover.png
  ```

  ### Step 3: Add the Markdown file

  Use this format:

  ```md
  ---
  title: My New Blog Post
  image: images/blog/my-new-blog-post/cover.png
  tags:
    - blog
    - project update
  excerpt: A short summary that appears in the blog listing.
  ---

  <!-- excerpt start -->
  Write a short opening summary here.
  <!-- excerpt end -->

  ## Overview

  Write the full blog post in Markdown.
  ```

  ### Important notes

  - The filename **must** follow the `YYYY-MM-DD-title.md` format
  - The post goes in `/_posts/`
  - `title`, `image`, and `excerpt` should be set in the front matter
  - If you provide an `image`, it is used in the blog listing
  - The blog page updates automatically from files in `/_posts/`

  ### Optional starting point

  You can also copy and edit:

  ```text
  /_posts/2026-06-04-sample-blog-post.md
  ```

  ---

  ## 5) Optional local check

  If you want to verify the site locally after making content updates:

  ```bash
  bundle install
  bundle exec jekyll build
  ```

  That confirms the site still builds successfully with your new content.
