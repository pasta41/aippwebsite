# Relax ML Lab website

This is the website of our research group, led by Chris De Sa, at Cornell University.

## Updating the home page
To update the text or carousel images, directly change `home.md`. Refer to that file for more details.

---
Most other relevant text changes get rendered through the yml files in the `_data` directory. The yml files each get rendered in order (from top to bottom), so pay attention to that when moving entries around. You can put html styling directly into the yml field values.

## Updating your team member profile
- The current list of team members is alphabetized by last name. Please adhere to this ordering for now. We can always change it.
- Update the entry associated with your name in `_data/team_members.yml`
- If you wish to update your photo, make sure to add the new image to the `images/teampic/` directory and make sure the file name for the `photo` yml field aligns with the new file. 

## Adding news
- Add an entry to the **bottom** of `_data/news.yml`.
- Provide the `date` in a format consistent with the other entries in the yml file.
- Provide the news update in the `headline` field. You can put html directly into this field to include styling, links, images, etc...	

## Adding a publication
- For a new publication, add an entry to the **top** of `_data/publist.yml`
- If you're adding a past publication, make sure you sort it appropriately / place it appropriately given its publication date. The yml file gets rendered in order of appearance.
- If you want to have your paper included in the **Highlights** section in addition to the **Full List**, please remember to include `highlight: 1` in your yml entry, a `description` (which can just be the paper abstract), an `image` file name (and put the corresponding image of that name in the `images/pubpic` directory), and (if appropriate) an `award` field for spotlights, orals, etc...

---
We have forked the Allan Lab Jekyll rep, from which the rest of this README is copied:

>This website is powered by Jekyll and some Bootstrap, Bootwatch. We tried to make it simple yet adaptable, so that it is easy for you to use it as a template. Plese feel free to copy and modify for your own purposes.  You don't have to link to us or mention us (but of course we appreciate it).

>Go to *aboutwebsite.md*  to learn how to copy and modidy this page for your purpose. 


>Copyright Allan Lab. Code released under the MIT License.

