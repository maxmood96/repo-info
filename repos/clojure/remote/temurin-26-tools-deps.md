## `clojure:temurin-26-tools-deps`

```console
$ docker pull clojure@sha256:2d5cd6d7bb1bc41f5ab3b5ed88d430a052e2bb3214dd5cf4e2f413a9c7b02570
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-26-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:9e1ddd7277f05fd15908b81ba9acf8259c2e6338d074fef56eea86365d3961a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224111852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b530c61751979dfa2f7711039d027fb826ffcac1b00676b24a6718f0a83b8a6d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:20:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:20:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:20:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:20:21 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:20:21 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:20:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:20:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:20:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:20:35 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:20:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4642b3240eb5e5226e64f921c2688de5e9b6c93e4eea4241af12e67a6f8e6393`  
		Last Modified: Fri, 08 May 2026 20:20:59 GMT  
		Size: 94.5 MB (94455680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e796e84e9851d25ff1614c2f858a0825377b0ac9cd3c4e9a4c8b80f771d7159`  
		Last Modified: Fri, 08 May 2026 20:20:59 GMT  
		Size: 81.2 MB (81166451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a07a0d3221aa607a88501fadc01b57e811cdf190effac89d817042b1211c7fb`  
		Last Modified: Fri, 08 May 2026 20:20:56 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98b4ebd79387b7ed16ce96591e9ce097bac950a471c2f282181bfa20360f3c9`  
		Last Modified: Fri, 08 May 2026 20:20:56 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:83936be22460b50ed1cc5edd22932012b136ea60aebd281e9e5f62d007945924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7360944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c1b092ec5c7468dc947e8a658593019158d6828c9fdaa71e100484a94aec21`

```dockerfile
```

-	Layers:
	-	`sha256:fcbe1f01a0dd80eb4654609dda2337123b727eb4a27eccca002a6f1b72dcd0e0`  
		Last Modified: Fri, 08 May 2026 20:20:56 GMT  
		Size: 7.3 MB (7344490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2b62c64266e78ce0b77cfa215933d288def9211093c73a6a26271c62d1548ef`  
		Last Modified: Fri, 08 May 2026 20:20:56 GMT  
		Size: 16.5 KB (16454 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dfb7f72d4f5a44f253d2df4e6211b4bdd445947c09f5e0698274d8551563fc16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222943804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a35c6371ec933f2f2a79fa0944415701da9e696251bf39f0f19d107173b0416`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:24:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:24:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:24:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:24:53 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:24:53 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:25:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:25:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:25:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:25:09 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:25:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4e16e0d283a3a3eb239e49d1a5246b2d195d07b1bee367e491655a28a453fc`  
		Last Modified: Fri, 08 May 2026 20:25:33 GMT  
		Size: 93.4 MB (93395166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b69caf10b9226bde14106cec9dd4f0b9652336a31773bdf0615ed71f611c10`  
		Last Modified: Fri, 08 May 2026 20:25:32 GMT  
		Size: 81.2 MB (81174446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25eb5f512fcfc500fe5f9db95bdb8b86b8adf26864cf81826526d47e4f96f68`  
		Last Modified: Fri, 08 May 2026 20:25:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793a8b3e8b7a17ce2ed48562ed5594a68956b987d9412decf3cd4db81dc5c472`  
		Last Modified: Fri, 08 May 2026 20:25:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:cbd042cc3a4a2490ae6f2fc2ef0999609669d7fb9e1a8a88bbfbd857ea50df59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7366871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85beada6851de7de8bf4b50e75ea7fbc3917ad452420e46d8a95ae672a85dd11`

```dockerfile
```

-	Layers:
	-	`sha256:3eb087a681a4c01cfcc4adc49f59a2c27a9b00c3d2c743aefbf7ee4ef82e033a`  
		Last Modified: Fri, 08 May 2026 20:25:30 GMT  
		Size: 7.4 MB (7350274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5475aa2967a2fc0c1e1d74b3824f7f5280b35d34fd3f20de0b02b63c0821342`  
		Last Modified: Fri, 08 May 2026 20:25:29 GMT  
		Size: 16.6 KB (16597 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps` - linux; ppc64le

```console
$ docker pull clojure@sha256:f7a8828b83394c6e5370fd8087fdf82472b494b2c2c7815908b5a018c9c264d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233123343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea03686221282cbbcc369872405c6381e66df66d1c5d15d179a6012e1703d60`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 08:50:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:50:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:50:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:50:35 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 08:50:36 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:54:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 08:54:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 08:54:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 08:54:35 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 08:54:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7799edd1fe5a978cb7609406a0fd100a731ce723a98e963f7a1829eaf333b6ef`  
		Last Modified: Wed, 22 Apr 2026 08:51:55 GMT  
		Size: 93.8 MB (93781443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77872afea176b5642ecd4f70e031daec7cc7650377859b1f5a62e7652f893fc1`  
		Last Modified: Wed, 22 Apr 2026 08:55:14 GMT  
		Size: 87.0 MB (87004126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48e804164d7922fa057d2573ce3220690e562178c9d04080975729e3f0a8a39`  
		Last Modified: Wed, 22 Apr 2026 08:55:11 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6150842d272552dcbcdd80494746fe30c4c12eef1beaad1ad34e8bbd210d4bd1`  
		Last Modified: Wed, 22 Apr 2026 08:55:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:8b33f1deb21e8e080cc7fe07be2c2086ef2975ec9f7a89f4c8aca36e03d6b8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7350169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8d298c2050a986bc54e45f4454613e47ab3533705c5275685d647fb1043841`

```dockerfile
```

-	Layers:
	-	`sha256:e3b296c3eacee81b5fe7154f1a54ad227c8f7d3ebb44c098702e81d685ba352d`  
		Last Modified: Wed, 22 Apr 2026 08:55:12 GMT  
		Size: 7.3 MB (7333654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32d772b46b9310d610fe93f48bcab03a674ee7212f30296038b3b818836e39e9`  
		Last Modified: Wed, 22 Apr 2026 08:55:11 GMT  
		Size: 16.5 KB (16515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps` - linux; s390x

```console
$ docker pull clojure@sha256:e8640ed2e160d7f03da515bf34c91443341c85a05af433e0d340a87561b7853f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217677611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286024e2f6f03f5f99a3a1803d8c993c7736e32354d51e6b76af7f211c108411`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:20:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:20:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:20:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:20:47 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 22:20:47 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:21:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 22:21:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 22:21:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:21:56 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:21:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71654bf0ab948d70880e532471e7b5acc4ab064c04bad172dfabf218407becc6`  
		Last Modified: Fri, 08 May 2026 22:21:25 GMT  
		Size: 90.5 MB (90547709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9721cab0898e50ced68ece2f80ed4352e77ccc5561882540026d1d96fce0550a`  
		Last Modified: Fri, 08 May 2026 22:22:22 GMT  
		Size: 80.0 MB (79980834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec5e2c3793b875c64aea2fe9beeb00b729fe9c97e1e3837328f2ce451878c83`  
		Last Modified: Fri, 08 May 2026 22:22:20 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb77262d69f4027b34d1a6653a2d3274f7851ad08ec6de9cd6fcd8b9fd64d8e0`  
		Last Modified: Fri, 08 May 2026 22:22:21 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:8a8ddbf54be0ccea0314d981682c16d02d9fb6c3a962163417e4641949acfc44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7337450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fbeec94527f1b6a54621e4a173d791a27588835faeb32c5d57650c4891765e0`

```dockerfile
```

-	Layers:
	-	`sha256:b069a157b9d0111e2cd2e02ffe3ab0f7d0b91e69ecf6741a4d372dfd155469ad`  
		Last Modified: Fri, 08 May 2026 22:22:21 GMT  
		Size: 7.3 MB (7320995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a82fd69c6af6f9fbadc75d1702b8cd5e1b015ab1c2bd86e51b0895e27dfe311f`  
		Last Modified: Fri, 08 May 2026 22:22:20 GMT  
		Size: 16.5 KB (16455 bytes)  
		MIME: application/vnd.in-toto+json
