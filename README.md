# matlab-style-guide

Collection of proposed MATLAB style guides, naming conventions, and recommendations.

## Background

Each program generally has set standard for coding stlye and naming conventions. However, **MATLAB does not** have an established company or community standard. There have been efforts to develop and agree on a standard, like [PEP8][pep8-style], but some of these resources are conflicting and are scattered across websites and forums.

Here, I hope to maintain a library of resources and recommendations to

1. Easily find relevant information regarding style and naming conventions
2. Propose or develop a community-agreed standard

Additional background information can be found [here](#additional-background).

## Style-Guide

Briefly, most of the previously developed style guides and naming convention documents are inspired by the same 2 or 3 sources.

- [MATLAB Style 2.0][matlab-style-2.0]
- [Elements of MATLAB Style][elements-matlab-style] with [updates][elements-matlab-style-updates]
- [MATLAB Programming Style Guide][programming-style-guide]

For more downloadable or linked resources, see [Resources](#resources).

### Proposed

Although there are several important considerations for a [complete style-guide][proposed-style-guide], below are the proposed naming conventions.

| Type             | Naming Convention              |
| ---------------- | ------------------------------ |
| Variables        | camelCase                      |
| Functions        | camelCase                      |
| Scripts          | camelCase                      |
| Classes          | PascalCase                     |
| Class Properties | camelCase                      |
| Class Methods    | camelCase                      |
| Packages         | lowercase (short, if possible) |
| Global           | UPPERCASE, UPPER_SNAKE_CASE    |
| Constant         | UPPERCASE, UPPER_SNAKE_CASE    |

A complete proposed style-guide can be found [here][proposed-style-guide] - Do not want to bore with all the details upfront :)

> The guide will also provide  information for *why* these conventions were selected.

<!-- > Consider applying the [PEP8][pep8-style] to your MATLAB code. Most recommendations will follow existing MATLAB conventions and/or previously community developed styles or see [Alternative Style-Guides](#alternative-style-guides). -->

### Recommendations

If you do not like the proposed style conventions above, have questions, or have recommendations, please consider

- [Contributing](#contributing)
- [Starting a conversation](#contact)
- [Have a look at alternatives](#alternative-style-guides)

## Resources

Previously developed style-guides:

- [MATLAB Style 2.0][matlab-style-2.0]
- [MATLAB Programming Style Guide][programming-style-guide]
- [Elements of MATLAB Style][elements-matlab-style] with [updates][elements-matlab-style-updates]
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

### Additional Background

## Roadmap

- [ ] Develop Style-Guide
- [ ] Link relevant resources (style-guides, programming conventions, etc)
- [ ] Website?

## Contributing

## License

## Contact

<!-- links -->

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