kiji
====
Kiji is editor of report templates (for example birth certificate). It is a
simple webpage where you can put text labels, lines, rectangles and 
placeholder texts. Created report template then must be filled with data on 
server side, where placeholder texts are replaced with data and saved into 
PDF which can be send back to client.

Kiji uses HTML5 canvas for rendering, JSON and local storage to save reports.
Kiji itself focus only on editing, so there is no saving, loading, printing 
support. You would write your own anyway. Simple PHP demo how to use data 
from HTML form and then create PDF is/(will be) included.

Purpose of Kiji is to allow users of you IS to modify reports to some extent 
(e.g. moving labels here and there, changing color or thicknes of elements, 
removing unwanted texts, adding logos, etc.) without your (programmer) 
intervention.

Kiji had several predecessors, and all of them was terrible to use, so this 
time, I'll do my best to make it as simple and as much user friendly as 
possible.

Goals
-----
- Ergonomy. No matter how many features you add to wysiwyg editor, when core
editing functionality is hard to use, no new features will change that. 
I want Kiji to be simple and intuitive to use for new users.
- Simplicity. Focus on just editing. Nothing else. No saving, no user ACL, no
PDF generation.

Current state
-------------

Kiji is NOT yet suitable for real use. It currently has only 2 item types. Text
and line. Most of work being done now is polishing ergonomy and source
refactoring. Basic editing is not yet mastered and thus no new features will be
added until this basic editing is perfected.

![Screenshot of kiji from 2012-08-05, black are text and line objects, pink is guide background bitmap, tools and inspector is on the left, selected items are blue](https://raw.github.com/zirapha/kiji/master/screenshot.png)

Todo
----
- See kiji.html (press Help button) for actual todo

History
-------
- 2012/08/08 - Rounded cap of lines thicker than 1px.
               Line threshold at least 1.5 for high zoom.
               Option to disable line ortogonalization.
- 2012/08/07 - Added corner tune for multiple lines (v3).
               Fixed screenshot resolution for github and it's url.
- 2012/08/06 - Added screenshot of current version.
               Added corner tool (variant L and T)
- 2012/08/05 - Slider for white background overlay.
- 2012/07/23 - Fixed left movement.
               Fixed unselecting items by holding shift while click on selected item.
               In help tool ESC set previous tool.
               Visualize threshold.
               Threshold different for line and text and depends on zoom.
               Improved items moving by temporal threshold to prevent misclicks
               Fixed line drawing (closePath after stroke)
- 2012/07/15 - Changed zoom to wheel+rightclick(or shift).
               Menu position fixed (now always visible).
- 2012/07/12 - Cleaned up global variables.
               Binding for drawing and moving items.
               Renamed lineDrawItem to lineDraw, lineDraw to lineDrawPrimitive.
               Minor firefox fixes.
- 2012/07/11 - Added leaks.js to show global variables and functions.
- 2012/07/08 - Global variables grouped into kiji object.
               Cleaned itemSelect using report[].distance.
- 2012/07/07 - Fixed focus issues.
- 2012/07/06 - Fixed text width update after text resize using shift+up/down.
- 2012/06/15 - First working demo (lines, texts, basic editing).
- 2012/05/23 - Development started.


