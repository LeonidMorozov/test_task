Part 1 (required)

create a job on ruby to parse the page resource's test_page.html using nokogiri
  1. get all links from pages as array and print results
  2. get resource's details from the page:
    - `title` (from <H1>),
    - `description` (<p class="descr">),
    - `tags list` (comma/space separated list below description) as array
    and print resource's object (hash)

Part 2 (optional but good to be done)

Update your code by
1. setup a rails or ruby app (this step is optional, may save your time)
2. Create model `resource` with attrs: id, title, description
3. Create model `tag` with attrs: id, title
4. Create association between `resource` and `tag` models
5. Import resource with tags to DB from the test_page.html

Part 3 (optional)

Update your code by
1. setup a rails or ruby app with static html pages (put files to the folder `public` on rails app)
2. add `source_url` attr to `resource` model, source_url is link to the page of resource on the site
3. re-use the job to parse the site (localhost:3000) with all given html pages using background jobs with resque/sidekiq
Job should parse one single page, put resource with tags to DB, find new links and add new jobs to resque/sidekiq queue.
Job for each page should be called once.