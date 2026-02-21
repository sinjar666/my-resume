# AltaCV Class Documentation

## Introduction
AltaCV is a LaTeX document class designed for creating resumes and curricula vitae with a modern and flexible design. This documentation explains the commands, options, and environments provided by `altacv.cls` to help first-time users.

## Loading the Class
```latex
\documentclass{altacv}
```

### Options
- **`academicons`**: Obsolete; no effect.
- **`normalphoto`**: Ensures photos are not cropped into circles.
- **`ragged2e`**: Enables the `ragged2e` package for improved text justification.
- **`withhyper`**: Enables clickable hyperlinks using the `hyperref` package.

## General Styling
### Colors
- **Accent color**: `blue!70!black`
- **Emphasis color**: `black`
- **Heading color**: `black`
- **Body text color**: `black!80!white`

You can customize these colors using the `\colorlet` command.

```latex
\colorlet{accent}{your_color_choice}
```

### Fonts
- `\namefont`: `\Huge\bfseries`
- `\taglinefont`: `\large\bfseries`
- `\personalinfofont`: `\footnotesize\bfseries`
- `\cvsectionfont`: `\LARGE\bfseries`
- `\cvsubsectionfont`: `\large\bfseries`

## Creating the Header
### Name and Tagline
```latex
\name{Your Name}
\tagline{Your Tagline}
```

### Personal Info
```latex
\personalinfo{
    \email{your.email@example.com}
    \phone{+1234567890}
    \location{City, Country}
    \github{githubusername}
}
```

### Photos
```latex
\photo[diameter]{path_to_photo}
```
- `diameter`: Size of the photo.
- `path_to_photo`: File path to the image.

### Rendering the Header
```latex
\makecvheader
```

## Sections and Subsections
### Main Sections
```latex
\cvsection{Section Title}
```

### Subsections
```latex
\cvsubsection{Subsection Title}
```

## Events and Achievements
### Events
```latex
\cvevent{Title}{Subtitle}{Date}{Location}
```

### Achievements
```latex
\cvachievement{\faTrophy}{Achievement Title}{Details}
```

## Tags and Skills
### Tags
```latex
\cvtag{Tag Name}
```

### Skills with Ratings
```latex
\cvskill{Skill Name}{Rating (1-5)}
```

## Reference Information
```latex
\cvref{Referee Name}{Position}{Contact Information}
```

## Charts
### Wheel Chart
```latex
\wheelchart{outer_radius}{inner_radius}{values/colors/names}
```
- Example:
```latex
\wheelchart{3cm}{1.5cm}{20/accent/Skill A,30/body/Skill B}
```

## Styling Utilities
### Full-width Environment
```latex
\begin{fullwidth}
    Your content here.
\end{fullwidth}
```

### Dividers
```latex
\divider
```

## Hyperlinks and Fields
### Predefined Fields
- **Email**: `\email`
- **Phone**: `\phone`
- **Homepage**: `\homepage`
- **Twitter**: `\twitter`
- **LinkedIn**: `\linkedin`
- **GitHub**: `\github`
- **ORCID**: `\orcid`
- **Location**: `\location`

### Custom Fields
```latex
\NewInfoField{name}{icon}[hyperlink_prefix]
```
- Example:
```latex
\NewInfoField{portfolio}{\faGlobe}[https://]
\portfolio{yourportfolio.com}
```

## Example Usage
```latex
\documentclass[ragged2e,withhyper]{altacv}
\name{Jane Doe}
\tagline{Software Engineer}
\personalinfo{
    \email{jane.doe@example.com}
    \phone{+123456789}
    \github{janedoe}
    \linkedin{jane-doe}
    \location{New York, USA}
}
\photo[2cm]{photo.jpg}
\begin{document}
\makecvheader
\cvsection{Experience}
\cvevent{Job Title}{Company}{2015--2020}{New York, USA}
\cvachievement{\faTrophy}{Employee of the Year}{Awarded for outstanding performance.}
\cvsection{Skills}
\cvskill{Programming}{5}
\cvskill{Design}{4}
\end{document}
