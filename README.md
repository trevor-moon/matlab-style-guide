# MATLAB Style Guide

Collection of proposed MATLAB style guides, naming conventions, and recommendations.

## Contents

- [MATLAB Style Guide](#matlab-style-guide)
  - [Contents](#contents)
  - [Background](#background)
  - [Style Guide](#style-guide)
    - [Previous Works](#previous-works)
    - [My Recommendation](#my-recommendation)
  - [Resources](#resources)
  - [Additional Background](#additional-background)
  - [Roadmap](#roadmap)
  - [Contributing](#contributing)
  - [Contact](#contact)
  - [License](#license)

## Background

Each program generally has set standard for coding stlye and naming conventions. However, **MATLAB does not** have an established company or community standard. There have been efforts to develop and agree on a standard, like [PEP8][pep8-style], but some of these resources are conflicting and are scattered across websites and forums.

Here, I hope to maintain a library of resources and recommendations to

1. Easily find relevant information regarding style and naming conventions
2. Propose or develop a community-agreed standard

Additional background information can be found [here](#additional-background).

## Style Guide

**Disclaimer:** The [style guide][proposed-style-guide] in this project is my opinion. However, it follows most of the content/consensus in prior documentation.

### Previous Works

Briefly, most of the previously developed style guides and naming convention documents are inspired by the same 2 or 3 sources.

- [MATLAB Style 2.0][matlab-style-2.0]
- [Elements of MATLAB Style][elements-matlab-style] with [updates][elements-matlab-style-updates]
- [MATLAB Programming Style Guide][programming-style-guide]

For more downloadable or linked resources, see [Resources](#resources).

### My Recommendation

My complete style guide can be found [here][proposed-style-guide].

Do you disagree or see problems? Maybe questions or recommendations? Consider one or more of the following

- [Contributing](#contributing)
- [See alternatives](#resources)
- [Contact me](#contact)

## Resources

Previously developed style-guides:

- [MATLAB Style 2.0][matlab-style-2.0]
- [MATLAB Programming Style Guide][programming-style-guide]
- [Elements of MATLAB Style][elements-matlab-style] with [updates][elements-matlab-style-updates]
- [MATLAB Guidelines][matlab-guidelines]
- [PEP8][pep8-style]
- [Google Stlye Guides][google-style-guide]

Other useful resources:

- [Naming Conventions Wiki][naming-convention-wiki]
- [Coding Conventions Wiki][coding-convention-wiki]
- [Programming Style Wiki][programming-style-wiki]

GitHub projects:

- [Matlab Style Guidelines Cheat Sheet](https://github.com/jasonnicholson/Matlab-Style-Guidelines-Cheat-Sheet)
- [MatLab](https://github.com/jonellingsen/MatLab)
- [MATLAB Style](https://github.com/ishiikurisu/MATLAB-style)
- [Matlab Style Guide](https://github.com/eeberhard/matlab_style_guide)

## Additional Background

**Personal note**: I tend to spend a lot of time determining the *correct* semantics and style to use in my MATLAB projects, and the community either a) is divided in their recommendations or b) does not provide formal documentation. So, my goal was to create something both for myself and others to reference.

Historically, MATLAB has used `lowercase` for files in their developed toolboxes, with some instances of `camelCase` or `PascalCase`. To better distinguish user-defined files from MATLAB built-in, I follow `camelCase` or `snake_case` naming conventions. Moreover, I find it more clear for readability.

## Roadmap

- [ ] Develop comprehensive style-guide
- [x] Link relevant resources (style-guides, programming conventions, etc)

## Contributing

If you have any additional resources, recommendations, or proposed changes, please consider contributing by:

1. Submitting an issue
2. Fork and create a pull request with the desired change

All suggestions are encouraged and welcomed.

## Contact

Please contact me if you have any questions or suggestions about the project.

<a href="mailto:trevor.r.moon@gmail.com"><img src="https://img.shields.io/badge/Gmail-D14836?style=flat&logo=gmail&logoColor=white&color=blue" height="25"/></a>

<a href="https://discordapp.com/users/477451290469859339"><img alt="Discord" src="https://img.shields.io/badge/Discord-7289DA?style=flat&logo=discord&logoColor=white&color=blue" height="25"/></a>

## License

<a href="https://github.com/trevor-moon/matlab-style-guide/blob/main/LICENSE.md"><img alt="License" src="https://img.shields.io/github/license/trevor-moon/matlab-style-guide?style=flat&color=blue" height="25"/></a>

<!-- links -->
[matlab-guidelines]: https://github.com/nschloe/matlab-guidelines
[proposed-style-guide]: style_guide.md
[pep8-style]: https://www.python.org/dev/peps/pep-0008/
[matlab-style-2.0]: https://www.mathworks.com/matlabcentral/fileexchange/46056-matlab-style-guidelines-2-0
[elements-matlab-style]: https://www.amazon.com/Elements-Matlab-Style-Richard-Johnson-dp-0521732581/dp/0521732581/ref=mt_other?_encoding=UTF8&me=&qid=
[elements-matlab-style-updates]: https://www.mathworks.com/matlabcentral/fileexchange/36540-updates-to-the-elements-of-matlab-style
[programming-style-guide]: https://sites.google.com/site/matlabstyleguidelines/home?authuser=0
[naming-convention-wiki]: https://en.wikipedia.org/wiki/Naming_convention_(programming)#Language-specific_conventions
[coding-convention-wiki]: https://en.wikipedia.org/wiki/Coding_conventions#Common_conventions
[programming-style-wiki]: https://en.wikipedia.org/wiki/Programming_style
[google-style-guide]: https://google.github.io/styleguide/
