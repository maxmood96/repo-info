## `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm`

```console
$ docker pull clojure@sha256:5937300af14ceb0807644e48e06e7a4b197534eceaf48f1e8efe23129d1320f7
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

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm` - linux; amd64

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

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

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

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

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

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:d6424416915ded4d38deb6ed5939c494ba5ad7b7ea519df365325a10c751ec9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233123730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7ac46e8433821f3f08d1069961a7703dcf42df3b46a07c3076f9b2f7098595`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:46:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:46:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:46:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:46:54 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 09 May 2026 02:46:54 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:50:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 09 May 2026 02:50:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 09 May 2026 02:50:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 09 May 2026 02:50:03 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 09 May 2026 02:50:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c82bc18c543cfc7a609b53543d15f2cb535420968abe79adcd8cc8351b5f32b`  
		Last Modified: Sat, 09 May 2026 02:47:58 GMT  
		Size: 93.8 MB (93781452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c55c343215c276be34f7bf18d214d333f7659dbe027d34cdba7c018d0b5324a`  
		Last Modified: Sat, 09 May 2026 02:50:40 GMT  
		Size: 87.0 MB (87004449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a9ddfb935ae61d846ffcdbaafe70329303cd43595a5713482d6c04b6350a8f`  
		Last Modified: Sat, 09 May 2026 02:50:37 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b723f7d91fa72784571bc48f7662eb38b7c2b53a318ba9b7636a559d3c2e1396`  
		Last Modified: Sat, 09 May 2026 02:50:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:15da5062e2bbc3724ad6c32a1026f77eebaf587f0db58d9d37adab574677603c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7350169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e806d81452e949ba3f66184c337c8566339eba93d5ebc93f0aad88df2a4eb8d0`

```dockerfile
```

-	Layers:
	-	`sha256:fabc49413b80f2cb44721a39e40eb96440894ac61500d2bd270f588d6281ec04`  
		Last Modified: Sat, 09 May 2026 02:50:38 GMT  
		Size: 7.3 MB (7333654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1f5d88e292ae64727a51c359d6e8dd1de640df3684b1f05bbf1a3f1db047a1d`  
		Last Modified: Sat, 09 May 2026 02:50:37 GMT  
		Size: 16.5 KB (16515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm` - linux; s390x

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

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

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
