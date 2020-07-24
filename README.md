# Wikipedia DOM order size tests

* http-head: 1,060 bytes (1.06kB)
* html-content-first (to end of first paragraph including infobox): 7,442 bytes (7.442 kB gzipped) 
* html-header-first (to end of first paragraph with lang links in sidebar): 20,179 bytes (20.179 kB gzipped)
* html-header-first-without-langlinks (to end of first paragraph without lang links in sidebar): 9,911 bytes (9.911 kB gzipped)

**Conclusion**: Even with the header, sidebar, article toolbar, and personal menu
ordered before the content in the DOM, we still are well under the 14kB budget
mentioned in T231168 when we remove the langlinks from the sidebar (which we
plan to do with the Desktop Improvements Project )[1]. 


[1] https://phabricator.wikimedia.org/T231168
