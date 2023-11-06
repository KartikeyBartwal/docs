# TensorFlow Documentation

<div align="center">
  <img src="https://www.tensorflow.org/images/tf_logo_horizontal.png"><br><br>
</div>

These are the source files for the guide and tutorials on
[tensorflow.org](https://www.tensorflow.org/overview).

## Image-Scaling Attacks: Protecting Your Machine Learning Models

**Description of Issue:**
TensorFlow is vulnerable to image-scaling attacks if specific scaling algorithms and parameters are used. These attacks
allow an adversary to arbitrarily change the output image of a downscaling operation. It is a threat for machine learning applications, similar to adversarial examples.

**Background:**
Downscaling is an important step in machine learning, as deep neural networks usually expect small fixed-sized inputs. An adversary can control the output of the downscaling step by slightly manipulating the input image, creating a security risk for machine learning models.

**Recommendations:**
We recommend users to be aware of the risk of scaling attacks when using TensorFlow for image scaling. TensorFlow provides vulnerable scaling algorithms such as nearest, bilinear, or bicubic scaling in the default settings, which may leave certain pixels unaltered, making the attack less noticeable.

To prevent image-scaling attacks in TensorFlow, we suggest using area scaling or setting `antialias = True` with TensorFlow 2.x. For older TensorFlow versions, only area scaling is recommended to prevent the attack.

For more details and examples, please visit our project website [scaling-attacks.net](https://scaling-attacks.net). You can also refer to our research paper [1] presented at the USENIX Security Symposium for a detailed analysis and possible defenses.

**Learn More:**
- [Project Website](https://scaling-attacks.net)
- [Research Paper: Adversarial Preprocessing](https://scaling-attacks.net/ResearchPaper.pdf)

To contribute to the TensorFlow documentation, please read
[CONTRIBUTING.md](CONTRIBUTING.md), the
[TensorFlow docs contributor guide](https://www.tensorflow.org/community/contribute/docs),
and the [style guide](https://www.tensorflow.org/community/contribute/docs_style).

To file a docs issue, use the issue tracker in the
[tensorflow/tensorflow](https://github.com/tensorflow/tensorflow/issues/new?template=20-documentation-issue.md) repo.

And join the TensorFlow documentation contributors on the
[docs@tensorflow.org mailing list](https://groups.google.com/a/tensorflow.org/forum/#!forum/docs).

## Community translations

[Community translations](https://www.tensorflow.org/community/contribute/docs#community_translations)
are located in the
[tensorflow/docs-l10n](https://github.com/tensorflow/docs-l10n) repo. These docs
are contributed, reviewed, and maintained by the community as *best-effort*. To
participate as a translator or reviewer, see the `site/<lang>/README.md`, join
the language mailing list, and submit a pull request.

## License

[Apache License 2.0](LICENSE)
