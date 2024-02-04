If you use the following:

=IMPORTDATA("https://raw.githubusercontent.com/mcgilvery-allison/testRepo/main/data.csv")

in a cell in google sheets, it'll automatically update (though not instantly) when changes are made the the data.csv file in this repository



this is just for a theoretical game though and there won't be anything useful as of current



the idea here was to make a set of files in google sheets that I could have be effectively a template that I could have friends make a copy of and they'd be able to play a game I made (almost) entirely in google sheets

the issue is that they'd have to re-input all of their data or some other janky user-side nonsense if I wanted to "update" the game (ie. add more enemy variety)

this is pretty much the culmination of my solution

at first, I was going to have it be to where I would use sheets' IMPORTRANGE function to import directly from a spreadsheet I could maintain

however, I ran into a couple of issues with this method:

- there would't be an easy way to expand the range of the data without, again, some user-side jank
 
- I would also have to manually give each person view access to the original document or something for it to export the data from (but they'd probably already have that b/c of having the template, but ehh)
  
I then thought well what if I used a .csv file with the IMPORTDATA function to solve the first issue, because the csv file itself would determine how many cells needed to be taken up in the spreadsheet (without having to keep copying thousands of empty cells)

so I tried making a csv file and uploading to my drive but I couldn't get the IMPORTDATA function working with a link to a file on my drive, so I decided to try github next

as I'm typing this I also realize that this has the benefit of not constantly sending minor updates to every google sheet that would use the import, but I could modify the csv locally and just push/commit updates when there was a noteworthy sum of things
