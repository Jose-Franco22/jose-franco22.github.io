:root {
    /* Add these styles to your global stylesheet, which is used across all site pages. You only need to do this once. All elements in the library derive their variables and base styles from this central sheet, simplifying site-wide edits. For instance, if you want to modify how your h2's appear across the site, you just update it once in the global styles, and the changes apply everywhere. */
    --primary: #ff6a3e;
    --primaryLight: #ffba43;
    --secondary: #ffba43;
    --secondaryLight: #ffba43;
    --headerColor: #1a1a1a;
    --bodyTextColor: #4e4b66;
    --bodyTextColorWhite: #fafbfc;
    /* 13px - 16px */
    --topperFontSize: clamp(0.8125rem, 1.6vw, 1rem);
    /* 31px - 49px */
    --headerFontSize: clamp(1.9375rem, 3.9vw, 3.0625rem);
    --bodyFontSize: 1rem;
    /* 60px - 100px top and bottom */
    --sectionPadding: clamp(3.75rem, 7.82vw, 6.25rem) 1rem;
}

body {
    margin: 0;
    padding: 0;
}

*, *:before, *:after {
    /* prevents padding from affecting height and width */
    box-sizing: border-box;
}

.cs-topper {
    font-size: var(--topperFontSize);
    line-height: 1.2em;
    text-transform: uppercase;
    text-align: inherit;
    letter-spacing: .1em;
    font-weight: 700;
    color: var(--primary);
    margin-bottom: 0.25rem;
    display: block;
}

.cs-title {
    font-size: var(--headerFontSize);
    font-weight: 900;
    line-height: 1.2em;
    text-align: inherit;
    max-width: 43.75rem;
    margin: 0 0 1rem 0;
    color: var(--headerColor);
    position: relative;
}

.cs-text {
    font-size: var(--bodyFontSize);
    line-height: 1.5em;
    text-align: inherit;
    width: 100%;
    max-width: 40.625rem;
    margin: 0;
    color: var(--bodyTextColor);
}

/*-- -------------------------- -->
<---          Services          -->
<--- -------------------------- -*/

/* Mobile - 360px */
@media only screen and (min-width: 0rem) {
    #services-448 {
        padding: var(--sectionPadding);
    }

        #services-448 .cs-container {
            width: 100%;
            /* changes at 1280px at tablet */
            max-width: 34.375rem;
            margin: auto;
            display: flex;
            flex-direction: column;
            align-items: center;
            /* 48px - 64px */
            gap: clamp(3rem, 6vw, 4rem);
        }

        #services-448 .cs-content {
            /* set text align to left if content needs to be left aligned */
            text-align: center;
            width: 100%;
            display: flex;
            flex-direction: column;
            /* centers content horizontally, set to flex-start to left align */
            align-items: center;
        }

        #services-448 .cs-card-group {
            width: 100%;
            padding: 0;
            margin: 0;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            /* 16px - 20px */
            column-gap: clamp(1rem, 1.5vw, 1.25rem);
            /* 24px - 60px */
            row-gap: clamp(1.5rem, 5vw, 3.75rem);
        }

        #services-448 .cs-item {
            list-style: none;
            width: 100%;
            max-width: 22.5rem;
            /* changes at desktop */
            padding-top: 9rem;
            position: relative;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

            #services-448 .cs-item:hover .cs-picture img {
                transform: scale(1.2);
                opacity: 0.4;
            }

            #services-448 .cs-item:hover .cs-flex:before {
                opacity: 1;
            }

        #services-448 .cs-picture {
            width: 100%;
            /* changes at desktop */
            height: 15.625rem;
            border-radius: 0.5rem;
            background-color: var(--primary);
            /* clips the corners of the image */
            overflow: hidden;
            display: block;
            position: absolute;
            top: 0;
            left: 0;
            z-index: -1;
        }

            #services-448 .cs-picture img {
                position: absolute;
                top: 0;
                left: 0;
                height: 100%;
                width: 100%;
                /* makes it behave like a background image */
                object-fit: cover;
                /* positions top of image to the top of the container */
                object-position: top;
                transition: transform 0.9s, opacity 0.5s;
            }

        #services-448 .cs-flex {
            text-align: center;
            width: 88%;
            padding: 0 1.5rem 1.5rem 1.5rem;
            /* prevents padding and border from affecting height and width */
            box-sizing: border-box;
            border: 1px solid #dad9e3;
            border-radius: 0.75rem;
            background-color: #fff;
            box-shadow: 0px 24px 54px rgba(87, 107, 147, 0.12);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            position: relative;
        }

            #services-448 .cs-flex:before {
                /* hover border box */
                content: "";
                background: transparent;
                /* prevents the mouse from interacting with it */
                pointer-events: none;
                border: 4px solid var(--primary);
                border-radius: 0.75rem;
                /* prevents border from affecting height and width */
                box-sizing: border-box;
                opacity: 0;
                position: absolute;
                display: block;
                top: -1px;
                left: -1px;
                right: -1px;
                bottom: -1px;
                transition: opacity 0.5s;
            }

        #services-448 .cs-wrapper {
            /* 80px - 120px */
            width: clamp(5rem, 9.2vw, 7.5rem);
            height: clamp(5rem, 9.2vw, 7.5rem);
            /* 20px - 24px */
            margin: 0 0 clamp(1.25rem, 1.5vw, 1.5rem);
            /* we use the same clamp value for height & width, but multiple by -.5 so it will be a negative value, and be half of the height.  Negative margins pull things toward the element so they overlap them, in this case we want the .cs-wrapper to overlap .cs-flex by half its height, so we use the same clamp for height and half it for the margin top value */
            margin-top: calc(clamp(5rem, 9.2vw, 7.5rem) * -0.5);
            border-radius: 50%;
            border: 4px solid var(--primary);
            background-color: #fff;
            /* prevents border from affecting height and width */
            box-sizing: border-box;
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
            z-index: 10;
        }

        #services-448 .cs-icon {
            /* 48px - 64px */
            width: clamp(3rem, 4.3vw, 4rem);
            height: auto;
            display: block;
        }

        #services-448 .cs-h3 {
            /* 20px - 25px */
            font-size: clamp(1.25rem, 1.9vw, 1.5625rem);
            line-height: 1.2em;
            font-weight: 700;
            margin: 0 0 0.5rem 0;
            color: var(--headerColor);
        }

        #services-448 .cs-item-text {
            /* 14px - 16px */
            font-size: clamp(0.875rem, 1.5vw, 1rem);
            line-height: 1.5em;
            font-weight: 400;
            /* 20px - 24px */
            margin: 0 0 clamp(1.25rem, 1.5vw, 1.5rem);
            color: var(--bodyTextColor);
        }

        #services-448 .cs-link {
            /* 16px - 20px */
            font-size: clamp(1rem, 1.5vw, 1.25rem);
            line-height: 1.5em;
            font-weight: 700;
            text-transform: uppercase;
            text-decoration: none;
            margin: 0;
            color: var(--primary);
            display: inline-block;
            position: relative;
        }

            #services-448 .cs-link:hover:before {
                width: 100%;
            }

            #services-448 .cs-link:before {
                /* animated underline */
                content: "";
                width: 0%;
                height: 3px;
                background: currentColor;
                opacity: 1;
                position: absolute;
                display: block;
                bottom: -0.125rem;
                left: 0;
                transition: width 0.3s;
            }
}
/* Tablet - 768px */
@media only screen and (min-width: 48rem) {
    #services-448 .cs-container {
        max-width: 80rem;
    }

    #services-448 .cs-card-group {
        flex-direction: row;
    }

    #services-448 .cs-item {
        width: 47%;
    }
}
/* Small Desktop - 1024px */
@media only screen and (min-width: 64rem) {
    #services-448 .cs-card-group {
        flex-wrap: nowrap;
    }

    #services-448 .cs-item {
        width: 100%;
        /* 144px - 274px */
        padding-top: clamp(9rem, 17.5vw, 17.125rem);
    }

    #services-448 .cs-picture {
        /* 224px - 428px */
        height: clamp(14rem, 28vw, 26.75rem);
    }
}





<!-- ============================================ -->
<!--                  Services                    -->
<!-- ============================================ -->

<section id="services-448">
    <div class="cs-container">
        <div class="cs-content">
            <span class="cs-topper">Services</span>
            <h2 class="cs-title">Landscaping Services in Sometown, USA</h2>
            <p class="cs-text">
                Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint. Velit officia consequat duis enim velit mollit. Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint. Velit officia consequat duis enim velit mollit.
            </p>
        </div>
        <ul class="cs-card-group">
            <li class="cs-item">
                <div class="cs-flex">
                    <picture class="cs-wrapper">
                        <img class="cs-icon" aria-hidden="true" loading="lazy" decoding="async" src="https://csimg.nyc3.cdn.digitaloceanspaces.com/Services/tree.svg" alt="icon" width="70" height="70">
                    </picture>
                    <h3 class="cs-h3">Service 1</h3>
                    <p class="cs-item-text">Lorem ipsum dolor sit amet, consectetur.</p>
                    <a href="" class="cs-link">Read More</a>
                </div>
                <picture class="cs-picture">
                    <source media="(max-width: 600px)" srcset="https://csimg.nyc3.cdn.digitaloceanspaces.com/Services/leaf.jpg">
                    <source media="(min-width: 601px)" srcset="https://csimg.nyc3.cdn.digitaloceanspaces.com/Services/leaf.jpg">
                    <img aria-hidden="true" loading="lazy" decoding="async" src="https://csimg.nyc3.cdn.digitaloceanspaces.com/Services/leaf.jpg" alt="leaf" width="345" height="428">
                </picture>
            </li>
            <li class="cs-item">
                <div class="cs-flex">
                    <picture class="cs-wrapper">
                        <img class="cs-icon" aria-hidden="true" loading="lazy" decoding="async" src="https://csimg.nyc3.cdn.digitaloceanspaces.com/Services/truck.svg" alt="icon" width="70" height="70">
                    </picture>
                    <h3 class="cs-h3">Service 1</h3>
                    <p class="cs-item-text">Lorem ipsum dolor sit amet, consectetur.</p>
                    <a href="" class="cs-link">Read More</a>
                </div>
                <picture class="cs-picture">
                    <source media="(max-width: 600px)" srcset="https://csimg.nyc3.cdn.digitaloceanspaces.com/Services/grass.jpg">
                    <source media="(min-width: 601px)" srcset="https://csimg.nyc3.cdn.digitaloceanspaces.com/Services/grass.jpg">
                    <img aria-hidden="true" loading="lazy" decoding="async" src="https://csimg.nyc3.cdn.digitaloceanspaces.com/Services/grass.jpg" alt="grass" width="345" height="428">
                </picture>
            </li>
            <li class="cs-item">
                <div class="cs-flex">
                    <picture class="cs-wrapper">
                        <img class="cs-icon" aria-hidden="true" loading="lazy" decoding="async" src="https://csimg.nyc3.cdn.digitaloceanspaces.com/Services/user.svg" alt="icon" width="70" height="70">
                    </picture>
                    <h3 class="cs-h3">Service 1</h3>
                    <p class="cs-item-text">Lorem ipsum dolor sit amet, consectetur.</p>
                    <a href="" class="cs-link">Read More</a>
                </div>
                <picture class="cs-picture">
                    <source media="(max-width: 600px)" srcset="https://csimg.nyc3.cdn.digitaloceanspaces.com/Services/leaves.jpg">
                    <source media="(min-width: 601px)" srcset="https://csimg.nyc3.cdn.digitaloceanspaces.com/Services/leaves.jpg">
                    <img aria-hidden="true" loading="lazy" decoding="async" src="https://csimg.nyc3.cdn.digitaloceanspaces.com/Services/leaves.jpg" alt="leaves" width="345" height="428">
                </picture>
            </li>
        </ul>
    </div>
</section>
