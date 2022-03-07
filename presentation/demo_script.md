# Script for pre-filmed specs-on-github demonstration

prep for recording videos:

- set resolution to 1920 x 1080, for humane-looking video
- remove `Variable Labels` heading from enrollment spec
- reinstate the 'play' typos

@kaiser-roy loads [the hcsrn-vdw repo](https://github.com/kaiser-roy/hcsrn-vdw) in chrome.

maybe point out that I am logged into the site as @kaiser-roy

Scrolls down to point out:

- (skip over initial grid of folders/files to start with)
- we are looking at readme.md--a MarkDown file, which gets displayed by default.
- pop the menu at the upper-left corner, which shows an auto-created menu based on the headings used in the document.
- show the list of tables & the ER diagram--both shamelessly stolen from the xlsx.
- The ER is a little small--click on it to reveal full-size version.
  - so we can show images--nice!
- Note the pencil icon on the upper-right--this lets us edit this main markdown file right through the GH website.
- the main tab is `Edit file`, but note that there's also `Preview`.
- Note that the tables list is numbered but only in the display
- the first few tables listed are actually hyperlinks to other markdown files in this project.
- cancel changes and follow the Enrollment spec link
  - here too we have a useful image
  - scroll down to the usage notes--nice that we can use a real bulleted list here (unlike excel)
  - this file is actually long enough to make that upper-right outline menu useful--zoom down to the 'foreign keys' and then back up to 'subject area description'
  - note that there's no heading for the variable list--let's add one!
  - pencil icon
  - note that it looks a little chaotic--change 'soft wrap' in upper-right to 'no wrap'
  - much better!
  - add the heading '## Variable List' immediately prior to the table.
  - show preview--looks nice
  - scroll down to commit changes. Use short description "added a heading for the 'variable list'"
  - click `commit changes` & note that the outline/menu has changed to match. Easy!
  - navigate back to the main repo & then the [commit list](https://github.com/kaiser-roy/hcsrn-vdw/commits/main).  See the newly-added commit at the top. It shows who and when the change was made. Click the commit description and you get a lovely side-by-side view of the before-and-after. This time we just changed one file but if we had changed multiple files they would all be listed one after another.
  - navigate back to the commit list--note that it lets you browse the project as it existed at any particular commit.

So--the project maintainer--@kaiser-roy in this case--can make changes directly through the web. No need for any special software.

How about others? One of the nice things about GitHub is the ease with which you can collaborate. Let's see what that looks like.

Switch to @alphonsederus2's screen.
Navigate to [hcsrn-vdw](https://github.com/kaiser-roy/hcsrn-vdw)

- follow link to enrollment page
- scroll down to plan_* vars--notice there's a typo in the Implementation Guidelines on these--**play** should be **plan** (the xlsx version of this spec actually has these typos BTW).
  - let's fix these.
  - notice that I have an 'edit' button too, even though I don't have write access to this project. Weird.
  - click pencil/edit button
  - note the banner advisory "You're making changes in a project you don't have write access to...".  What this means is that GitHub is automatically making a copy of the repo in @alphonsederus2's account, which is where these edits will go.
  - make the changes & scroll down.  Note the difference here--what had been 'Commit changes' when done by the project maintainer (@kaiser-roy) now says 'Propose changes'
  - Add the short desc 'Corrected some typos in the enrollment spec'  and click 'Propose changes'
  - this next page is a tiny bit complicated--but notice that it shows you a 'diff'--the portion of the file that actually changed with my edit.
  - notice you can view that diff 2 different ways--`Unified` which shows the old & new lines one after another in a single display, and `Split` which shows old/existing on the left and new/proposed on the right.  Note that the specific changed words are given an especially dark shade of red/green.
  - this looks good--it's got all our changes and only those changes we intended to make.  To convey this suggestion to the project maintainer, we click the 'create pull request' button.
  - now the page changes, giving us a box to type some additional comments into. This is optional, but friendly.  Type "Hey Roy--noticed a few typos in enrollment." and click the 'Create pull request' button.
  - at this point, Roy will get an e-mail from github notifying him of the pull request.  And notice that I can add more comments if I like, or I can think better of my proposal and 'close with comment'.

Switch to @kaiser-roy's screen. Open outlook and display the e-mail that was sent.

- click the link--we go right to the pull request.
- github let's me know that there are no conflicts with the existing project files. A conflict would have happened if someone else edited those very lines in some inconsistent way. But we have no problems here.
- click the 'Files changed' tab and notice I have the same exact 'diff' view that @alphonsederus2 was looking at.  This lets me see that yep, the only changes here are good ones.
- click back to the 'Conversation' tab and click 'Merge changes'.
- Notice we have to click a second time to confirm.
- All done! Navigate back to the enrollment spec and see that the changes are there.
- navigate to the commit list and notice that we have a new commit that memorializes the merged pull request.





