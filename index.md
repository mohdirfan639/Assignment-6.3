Assignment 6.3 — Overflow & Layout Fixing
1. Project structure
Create a folder named Assignment-6.3 containing these files:


text
Assignment-6.3/
├── index.html
└── style.css
2. HTML code — index.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 6.3 - Overflow & Layout Fixing</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header>
        <h1>CSS Overflow & Layout Fixing</h1>
        <p>Explore overflow properties and learn to fix layout issues.</p>
    </header>

    <main>
        <section class="section">
            <h2>1. Overflow: Visible</h2>
            <p>Content extends outside the container when necessary.</p>
            <div class="overflow-box visible-box">
                <p>
                    This is a demonstration of overflow visible. The container
                    has a fixed height, but the text continues beyond its
                    boundaries. No content is clipped, so the overflowing text
                    can overlap other page elements.
                </p>
                <p>
                    Additional content makes the overflow easy to observe.
                    The container does not automatically grow to fit this text.
                </p>
            </div>
        </section>

        <section class="section">
            <h2>2. Overflow: Hidden</h2>
            <p>Content outside the container is clipped.</p>
            <div class="overflow-box hidden-box">
                <p>
                    This is a demonstration of overflow hidden. The container
                    has a fixed height, and any content extending beyond its
                    boundaries is clipped and cannot be viewed by scrolling.
                </p>
                <p>
                    This extra paragraph is intentionally hidden when it
                    extends beyond the container.
                </p>
            </div>
        </section>

        <section class="section">
            <h2>3. Overflow: Auto</h2>
            <p>A scrollbar appears when the content needs it.</p>
            <div class="overflow-box auto-box">
                <p>
                    This is a demonstration of overflow auto. The container
                    has a fixed height and contains enough text to overflow.
                    A scrollbar appears when required so users can read the
                    complete content without changing the container size.
                </p>
                <p>
                    Scroll down to read this additional paragraph. Overflow
                    auto is useful for comments, articles, and other content
                    panels that must fit within a limited space.
                </p>
                <p>
                    This is the final paragraph. Keep scrolling to see all
                    the content inside the container.
                </p>
            </div>
        </section>

        <section class="section">
            <h2>4. Overflow: Scroll</h2>
            <p>Scrolling is enabled even if it is not needed.</p>
            <div class="overflow-box scroll-box">
                <p>
                    This is a demonstration of overflow scroll. The container
                    has a fixed height and displays scrollbars to allow users
                    to move through content that exceeds its boundaries.
                </p>
                <p>
                    More text is included to demonstrate scrolling. Use the
                    scrollbar or your mouse wheel to read the remaining text.
                </p>
                <p>
                    Scrollbars are reserved for this container even when
                    there is little or no overflowing content.
                </p>
            </div>
        </section>

        <section class="section">
            <h2>5. Second Scrollable Container</h2>
            <p>This container uses overflow: auto for a practical example.</p>
            <div class="article-box">
                <h3>Importance of CSS Layout</h3>
                <p>
                    CSS layout properties help organize content on a webpage.
                    A fixed-size content area can be useful when displaying
                    instructions, news, comments, or long descriptions.
                </p>
                <p>
                    When content exceeds the available space, overflow auto
                    allows users to access the remaining content using a
                    scrollbar when necessary.
                </p>
                <p>
                    Responsive design, appropriate widths, and correct
                    overflow settings prevent content from covering other
                    elements or extending beyond the viewport.
                </p>
                <p>
                    Always test the page on different screen sizes to make
                    sure that text remains readable and scrollbars work as
                    expected.
                </p>
            </div>
        </section>

        <section class="section">
            <h2>6. Overflow Issue and Fixed Layout</h2>
            <p>Compare the broken layout with the corrected version.</p>

            <h3>Before Fix: Broken Layout</h3>
            <div class="broken-layout">
                <div class="broken-card">
                    <h4>Problem Box</h4>
                    <p>
                        This box has a fixed width that is too large for its
                        parent. It causes horizontal overflow on small screens.
                    </p>
                </div>
            </div>

            <h3>After Fix: Responsive Layout</h3>
            <div class="fixed-layout">
                <div class="fixed-card">
                    <h4>Fixed Box</h4>
                    <p>
                        This box uses box-sizing and max-width to stay inside
                        its parent and fit smaller screens.
                    </p>
                </div>
            </div>
        </section>
    </main>

    <footer>
        <p>Assignment 6.3 | Overflow & Layout Fixing</p>
    </footer>

</body>
</html>
3. CSS code — style.css

css

/* General styling */
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    padding: 20px;
    font-family: Arial, sans-serif;
    line-height: 1.6;
    color: #1e293b;
    background-color: #f1f5f9;
}

/* Header */
header {
    padding: 25px;
    margin-bottom: 30px;
    text-align: center;
    color: white;
    background-color: #1d4ed8;
    border-radius: 12px;
}

header h1 {
    margin-top: 0;
}

/* Each demonstration section */
.section {
    max-width: 850px;
    margin: 0 auto 30px;
    padding: 20px;
    background-color: white;
    border: 1px solid #cbd5e1;
    border-radius: 10px;
}

.section h2 {
    color: #1d4ed8;
}

.section h3 {
    margin-top: 25px;
}

/* Common fixed-size containers */
.overflow-box {
    width: 100%;
    max-width: 500px;
    height: 150px;
    padding: 15px;
    border: 3px solid #2563eb;
    border-radius: 8px;
    background-color: #eff6ff;
}

/* 1. Visible: content can extend beyond the box */
.visible-box {
    overflow: visible;
    border-color: #16a34a;
    background-color: #f0fdf4;
}

/* 2. Hidden: overflowing content is clipped */
.hidden-box {
    overflow: hidden;
    border-color: #dc2626;
    background-color: #fef2f2;
}

/* 3. Auto: scrollbar appears when required */
.auto-box {
    overflow: auto;
    border-color: #2563eb;
    background-color: #eff6ff;
}

/* 4. Scroll: scrolling is always enabled */
.scroll-box {
    overflow: scroll;
    border-color: #9333ea;
    background-color: #faf5ff;
}

/* Second scrollable content container */
.article-box {
    width: 100%;
    max-width: 600px;
    height: 180px;
    padding: 15px;
    overflow: auto;
    border: 2px solid #0891b2;
    border-radius: 8px;
    background-color: #ecfeff;
}

.article-box h3 {
    margin-top: 0;
    color: #0e7490;
}

/* BEFORE FIX: deliberately broken layout */
.broken-layout {
    width: 100%;
    padding: 10px;
    border: 2px dashed #dc2626;
    background-color: #fef2f2;
}

/* Fixed width is too large for the parent */
.broken-card {
    width: 650px;
    max-width: none;
    padding: 20px;
    background-color: #fecaca;
    border: 3px solid #dc2626;
    border-radius: 8px;
}

/* AFTER FIX: responsive layout */
.fixed-layout {
    width: 100%;
    min-width: 0;
    padding: 10px;
    border: 2px dashed #16a34a;
    background-color: #f0fdf4;
}

/* Box now fits within the available space */
.fixed-card {
    width: 650px;
    max-width: 100%;
    padding: 20px;
    overflow-wrap: anywhere;
    background-color: #dcfce7;
    border: 3px solid #16a34a;
    border-radius: 8px;
}

/* Footer */
footer {
    padding: 15px;
    margin-top: 30px;
    text-align: center;
    color: #64748b;
}

/* Responsive layout */
@media (max-width: 600px) {
    body {
        padding: 10px;
    }

    header {
        padding: 15px;
    }

    header h1 {
        font-size: 24px;
    }

    .section {
        padding: 12px;
    }

    .overflow-box,
    .article-box {
        max-width: 100%;
    }
}
4. Expected output
The webpage will contain four overflow examples, a second scrollable article panel, and a before-and-after layout comparison.

CSS Overflow & Layout Fixing
Explore overflow properties and learn to fix layout issues.

1. Overflow: Visible
Content can extend beyond the container.

Additional content can overlap the area below.

2. Overflow: Hidden
Content outside the fixed-height box is clipped.

This paragraph is not accessible by scrolling.

3. Overflow: Auto
This container has a fixed height.

Extra content requires scrolling to read everything.

Overflow auto shows a scrollbar when necessary.

This is the final paragraph in the example.

4. Overflow: Scroll
Scrollbars are enabled for this box.

Read the extra content by scrolling.

The container keeps its fixed height.

End of the scroll example.

5. Layout Fixing
Before fix — broken width

Fixed width: 650px; may overflow its parent.

After fix — responsive width

max-width: 100%; fits the parent container.

Illustrative preview. Open your HTML file in Chrome to see the actual CSS behavior and browser scrollbars.
5. Understanding the four overflow values
CSS property

What it does

overflow: visible

Displays overflowing content outside the container.

overflow: hidden

Clips content that extends beyond the container.

overflow: auto

Adds scrollbars when content overflows.

overflow: scroll

Enables scrolling even when the content fits.

Important: In this assignment, each example uses a fixed height of 150px. This makes the differences between the overflow values easier to observe.

6. Overflow issue and solution
The broken example uses:


css
.broken-card {
    width: 650px;
    max-width: none;
}
On a narrow screen or inside a smaller parent, this width can cause horizontal overflow.

The corrected version is:


css
.fixed-card {
    width: 650px;
    max-width: 100%;
    box-sizing: border-box;
    overflow-wrap: anywhere;
}
The max-width: 100% rule prevents the card from becoming wider than its parent, while box-sizing: border-box keeps padding and borders within its specified width. overflow-wrap: anywhere allows long words or unbroken strings to wrap.

7. How to take the submission screenshots
Save both files in the Assignment-6.3 folder.

Open index.html in Google Chrome.

Take a screenshot showing all four overflow examples and the second scrollable container.

Take another screenshot showing the broken layout and the corrected layout.

Save them as:

overflow-examples.png

fixed-layout.png

8. Conclusion
CSS overflow properties control how content is displayed when it exceeds a container's dimensions. The visible, hidden, auto, and scroll values provide different ways to handle overflowing content. Using responsive widths, max-width, and box-sizing helps fix layout problems and keeps webpages usable on different screen sizes.