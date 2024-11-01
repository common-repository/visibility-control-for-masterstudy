=== Visibility Control for MasterStudy ===
Contributors: liveaspankaj
Donate link:
Tags: MasterStudy, eLearning, LMS, Hide Content, Hide Message
Requires at least: 4.0
Tested up to: 6.5.3
Stable tag: 1.0
Requires PHP: 5.6
License: GPLv2 or later
License URI: https://www.gnu.org/licenses/gpl-2.0.html

Visibility Control for MasterStudy LMS helps you hide messages and content for specific criterion anywhere on your WordPress page.

== Description ==

Visibility Control for MasterStudy helps you hide messages and content for specific criterion anywhere on your WordPress page.

You can show/hide HTML elements, menus, and other details based on:
1. User's access to a particular **MasterStudy LMS Course**,
2. User's course completion status of a particular **MasterStudy LMS Course**, Or
3. User is **Logged In** or **Logged Out**.
4. User's role.

You simply need to add a CSS class to your element div or span. As explained here:

**Example:**

Login/Logout Status:

* To show the element/menu item to a logged-in user, add this CSS class: **visible_to_logged_in** OR  **hidden_to_logged_out**
* To hide the element/menu item from a logged-in user, add this CSS class: **visible_to_logged_out** OR  **hidden_to_logged_in**

For user's role:
* To show the element/menu item to a user will role administrator, add this CSS class: **visible_to_role_administrator** OR **hidden_to_role_administrator**
* Note: To show an element to multiple specific roles only, you need add the element multiple times, one for each role. To hide an element/menu from specific multiple roles only you can add the element once add multiple classes to the same element.

If Course ID is 123

* To show the element/menu item to user with access to above Course, add this CSS class: **visible_to_course_123**
* To hide the element/menu item from user with access to above Course, add this CSS class: **hidden_to_course_123**
* To show the element/menu item to a logged-in user, add this CSS class: **visible_to_logged_in** OR  **hidden_to_logged_out**
* To hide the element/menu item from a logged-in user, add this CSS class: **visible_to_logged_out** OR  **hidden_to_logged_in**

For a course completion status, if Course ID is 123:

* To show the element/menu item to user who completed above course, add this CSS class: **visible_to_course_complete_123**
* To hide the element/menu item from user who completed above course, add this CSS class: **hidden_to_course_complete_123**
* To show the element/menu item to user who has not completed above course, add this CSS class: **visible_to_course_incomplete_123**
* To hide the element/menu item from user who has not completed above course, add this CSS class: **hidden_to_course_incomplete_123**

**Mechanism of Functioning**

* **Multiple CSS Classes:** If multiple visibility control classes are added, ALL of them must meet the criterion to keep the element visible. If any one of them hides the element, it will be hidden. For example: visible_to_course_123 visible_to_course_124 will show the element only to those who have access to both courses.
* Hidden data/elements reaches the browser. Though user's do not see it.
* CSS is added to the page for all CSS elements that needs to be hidden based on above rules.
* After page is loaded. These elements are removed from page using jQuery (if available), so it won't be available on Inspect.
* Elements rendered after the page load are hidden but not removed from DOM/page.

**Future Development**

Depending on the interest in this feature, we will decide on adding a shortcode and/or a Gutenberg Block to achieve this feature.

**Other Visibility Control Plugins:**
- [Visibility Control for LearnDash LMS](https://www.nextsoftwaresolutions.com/learndash-visibility-control/)
- [Visibility Control for WP Courseware LMS](https://www.nextsoftwaresolutions.com/visibility-control-for-wp-courseware/)
- [Visibility Control for LearnPress LMS](https://www.nextsoftwaresolutions.com/visibility-control-for-learnpress/)
- [Visibility Control for LifterLMS](https://www.nextsoftwaresolutions.com/visibility-controlfor-lifterlms/)
- [Visibility Control for TutorLMS](https://www.nextsoftwaresolutions.com/visibility-control-for-tutorlms/)
- [Visibility Control for Sensei LMS](https://www.nextsoftwaresolutions.com/visibility-control-for-sensei/)
- [Visibility Control for WooCommerce](https://www.nextsoftwaresolutions.com/woocommerce-visibility-control/)

**Related Plugins for MasterStudy LMS:**
- [Experience API for MasterStudy LMS](https://www.nextsoftwaresolutions.com/experience-api-for-masterstudy-lms/)

== Installation ==

This section describes how to install the plugin and get it working.

e.g.

1. Upload the plugin files to the `/wp-content/plugins/visibility-control-for-masterstudy` directory, or install the plugin through the WordPress plugins screen directly.
2. Activate the plugin through the 'Plugins' screen in WordPress
3. Add the CSS classes to your HTML elements or Menu Items as described in the Details section.

== Frequently Asked Questions ==

= What is MasterStudy LMS? =

MasterStudy LMS is a popular WordPress based Learning Management System (LMS) plugin. It includes many advanced features including, quizzing engine, course management, reports, certificates and payment methods.

You can also add GrassBlade xAPI Companion plugin and GrassBlade LRS to start using Experience API (xAPI) based contents with MasterStudy LMS.

== Screenshots ==

1. Show menu only to Loggout user
2. Show menu only to Logged In user (or Course access)
3. Show a message if user has access to course (using HTML anywhere)
4. Show a message if user doesn't have access to course (using Additional CSS class)

== Changelog ==

= 1.0 =
Initial Version
