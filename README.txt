#Route Finder Hypermedia Type

Note: Because a graphical geospatial interface seemed outside of the scope of this assignment, all route representations are treated simply as a list of latitude/longitude coordinates.

##Attribute Values

**ID attributes**

*content*
>Applied to a SECTION tag to distinguish it from the header and to mark it as a container of all other content on the page.

*routes*
>Applied to a SECTION tag to mark a list of routes.


**Class attributes**

*search*
>Applied to a FORM tag. A templated query link to search for routes matching specified criterea. The element must be set to FORM.method="get".

*new-route*
>Applied to a FORM tag. A non-idempotent update link that posts a new route with the specified metadata. The element must be set to FORM.method="post".

*update-route*
>Applied to a FORM tag. A non-idempotent update link that updates an existing route with the specified metadata. The element must be set to FORM.method="post".

*all*
>Applied to a UL tag. A list representation. When this element is a descendent of SECTION.id="routes", it may contain one or more LI.class="route" descendent elements.

*matching*
>Applied to a UL tag. A representation of a list of routes matching some search criteria. When this element is a descendent of SECTION.id="routes", it may contain one or more LI.class="route" descendent elements. 

*route*
>When applied to a LI tag, a representation of a listed route. Must contain only one SPAN.class="route-name" descendent element and one SPAN.class="username" descendent element.

>When applied to a SECTION tag, a representation of a route. Must contain H2.class="route-name", H3.class="username", SPAN.class="description", SPAN.class="trail-type", SPAN.class="trail-region", SPAN.class="trail-length", SPAN.class="trail-difficulty", and UL.class="coordinates" descendent elements. 

*route-name*
>Applied to a SPAN tag or H2 tag. Contains the name of a route.

*username*
>Applied to a SPAN tag or H3 tag. Contains the name of a user.

*description*
>Applied to a SPAN tag. Contains a text description of a route.

*trail-region*
>Applied to a SPAN tag. Contains the region of a route.

*trail-difficulty*
>Applied to a SPAN tag. Contains the difficulty of a route.

*trail-length*
>Applied to a SPAN tag. Contains the length of a route.

*trail-type*
>Applied to a SPAN tag. Contains the trail type of a route.

*coordinates*
>Applied to a UL tag. A list representation. When this element is a descendent of SECTION.id="route", it may contain one or more LI.class="route-point" descendent elements.

*route-point*
>Applied to a LI tag. A representation of one point in space on a particular route.Must contain a pair of SPAN.class="latitude" and SPAN.class="longitude" descendent elements.

*latitude*
>Applied to a SPAN tag. Represents the latitude of a particular point on a route.

*longitude*
>Applied to a SPAN tag. Represents the longitude of a particular point on a route.


**Name attributes**

*match-text*
>Applied to an INPUT[text] element. The user wants to see only routes that contain this text.

*trail-region*
>Applied to an INPUT[checkbox] element. The user wants to see routes that are in this region.

*trail-difficulty*
>When applied to an INPUT[checkbox] element and contained within a FORM.class="search" element, the user wants to see routes that have this difficulty level.

>When applied to an INPUT[radio] element and contained within a FORM.class="new-route" element, the difficulty of the new route.

*trail-length*
>Applied to an INPUT[checkbox] element. The user wants to see routes that have this length.

*trail-type*
>Applied to an INPUT[checkbox] element. When contained within FORM.class="search" element, the user wants to see routes that are of this trail type.

>When contained within a FORM.class="new-route" element, the trail type of the route.

*route-name*
>Applied to an INPUT[text] element. The name of the route.

*route-description*
>Applied to a TEXTAREA element. The description of the route.

*coordinates*
>Applied to a TEXTAREA element. The set of latitude/longitude points representing a route.


**Rel attributes**

*index*
>Applied to an A tag. A reference to the starting URI for the application.

*route*
>Applied to an A tag. A reference to a particular route representation.


