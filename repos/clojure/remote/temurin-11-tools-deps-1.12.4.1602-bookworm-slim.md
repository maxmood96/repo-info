## `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm-slim`

```console
$ docker pull clojure@sha256:8ebb901fa3338a8bc85c2ce4e4bc36352f07376c07b4358b9aa7537e3b010489
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

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:30e5bf2b312619a406d0dd958399f4f172cdd9d33a1653e38d09f283d6546594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243721536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97ee2dd2acf201a2f0ca9f95c9b8ac613045fca93d46fe9e375deba00196a66`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:53:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:53:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:53:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:53:54 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:53:55 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:54:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:54:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:54:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac9b998bbc7e0e221cbaa3131bdd5cc21fc9e066238fea5f6ad9c1f5bd83081`  
		Last Modified: Tue, 24 Feb 2026 19:54:32 GMT  
		Size: 145.8 MB (145806748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a285a8704d294701a783c3e1b5bef876b77078bf4512e0439f6c60c6c5ac5fc2`  
		Last Modified: Tue, 24 Feb 2026 19:54:31 GMT  
		Size: 69.7 MB (69677865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1949e0abe39c547ce85083f76d0044ca5ec3b35a23803044afeb5bca41a9cc`  
		Last Modified: Tue, 24 Feb 2026 19:54:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ceebdf136cb422d13f0444fb287e285aad4ce730f505efde9fdb8961f048e2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5149062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d8b0b97cf8472bed0ff9a4148ee0ffc755b13cca8b9a4073646788b20566bc6`

```dockerfile
```

-	Layers:
	-	`sha256:4fce8408a4309d89f2fc3c3aaefe8fae418764f321c31bb3f76f26b91712bb18`  
		Last Modified: Tue, 24 Feb 2026 19:54:29 GMT  
		Size: 5.1 MB (5134795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54a47a10cfb61b160db1d566ef9625fb1f27be64e32e986565e3a1d538e2f176`  
		Last Modified: Tue, 24 Feb 2026 19:54:28 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9dd27af98f35a85ec91a81722caa2d487d43ac57464dcd7c74b4611804374e26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240290925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca665d09ee056a2b952add3d392bc2cbce9c017c683242335761d1c1300a339`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:04:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:04:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:04:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:04:48 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:04:48 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:05:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:05:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:05:04 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5871f4fbe7dfcc9a36025e9899c39bea7d61c0cbee0950ee344fc1ad5ecb34e`  
		Last Modified: Tue, 24 Feb 2026 20:05:26 GMT  
		Size: 142.5 MB (142501445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff47636a43c4fb63663963bac7994cef190c77e04ced38dea31ca7299385e754`  
		Last Modified: Tue, 24 Feb 2026 20:05:24 GMT  
		Size: 69.7 MB (69672757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e6b144d0e3d97eab8459e45306b0951f5e3ee020e5ac0dd1b275941d015a58`  
		Last Modified: Tue, 24 Feb 2026 20:05:22 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:236fe691ac9d3ea8c4283b32189f964b936d356c35007d06641e4b054a5c6514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5155559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9372878196320d36304c859e00a4e914a71c7e3bb44db5fe1a17eba57617bba`

```dockerfile
```

-	Layers:
	-	`sha256:f18c6a72f628ddc8bcf6db1e0ca65390a206ef35174af19995cdca07bd52bfb4`  
		Last Modified: Tue, 24 Feb 2026 20:05:22 GMT  
		Size: 5.1 MB (5141174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b09242eca6d5763c458535ac10e72aa610bd909061655d5b7220e5edb03c04e0`  
		Last Modified: Tue, 24 Feb 2026 20:05:21 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:0e94b19881865e9c822522007314e2edc2cbafa5d15ed31206df3377a96934d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240590914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de92b6b82f092f7cab62ea404cc065ca0b169fa64bd976c9d82f335011dcc1bf`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 25 Feb 2026 01:49:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:49:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:49:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:49:21 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 25 Feb 2026 01:49:22 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 01:54:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 25 Feb 2026 01:54:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 25 Feb 2026 01:54:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9bc5a19266700a831a5467cc408599b98ef115eeaac770a91b7bf3a370d120`  
		Last Modified: Wed, 25 Feb 2026 01:50:54 GMT  
		Size: 133.0 MB (132997811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa2082da2ff541eea44fb5144ac7ba05dc362b16c234932147e212a0091dfec`  
		Last Modified: Wed, 25 Feb 2026 01:54:56 GMT  
		Size: 75.5 MB (75514124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a76df1d744e0a2c586d74ac432b3f644d5c40dce49c89a9c65702b0e988292`  
		Last Modified: Wed, 25 Feb 2026 01:54:53 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bc0269e50f14ba72c4f19a4ec9e174ebcb772b0c5efe11b127622438bb5493b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5153653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d74e04041f7eba35dc8c0eb8c2dd21071bb71c2ffd5fe3ad09a763592074deb7`

```dockerfile
```

-	Layers:
	-	`sha256:21367da68bcf365cf4adc7cf645b7d66e37ecb8373b55fd29e1903ea3b08b773`  
		Last Modified: Wed, 25 Feb 2026 01:54:53 GMT  
		Size: 5.1 MB (5139338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5452056fc5cd90934fbaaab5607676aabe86ef9cc6c0359ddee897be119944a`  
		Last Modified: Wed, 25 Feb 2026 01:54:53 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:fe59528ae68e25ab20d0fd5fdc2b5f36e9371dc0e1b1ec39605a3de33106c82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221944640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9839dedab67174e99ecc196d2e782472d79bd75633a84257ad86d54041b832`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 23:11:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:11:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:11:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:11:21 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 23:11:22 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:14:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 23:14:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 23:14:03 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88825d23886aad7630f698fabec26ff327fb5cc56e608c0be4067ab5b8f57c4`  
		Last Modified: Tue, 24 Feb 2026 23:12:49 GMT  
		Size: 126.6 MB (126562035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb7c616aa7454b07e97bcddcae7fed6f06813f94ccb3ef2285753919a26fdba`  
		Last Modified: Tue, 24 Feb 2026 23:14:35 GMT  
		Size: 68.5 MB (68490439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4aa5ebad521d42b3f7f34eb4141596b0ab984f039ab8d373aedac0d35938cc`  
		Last Modified: Tue, 24 Feb 2026 23:14:33 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e2434e8a4c044c241c3f1129141fd788eeae2fa318e7e34c3d60a349242f219d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5140387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579f8a2b94f40d98e6a8c210911194b4e21cd47c4d245b6968866065fa56b4cb`

```dockerfile
```

-	Layers:
	-	`sha256:5a2e6c5b5767eb5c56e3a36f1ce07aa25c9a97451226230d6e0440a08130b2c8`  
		Last Modified: Tue, 24 Feb 2026 23:14:33 GMT  
		Size: 5.1 MB (5126120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af9fd8d473964530daf841d36a3a4feb9beca276a0e7b96fb462890630aa67cc`  
		Last Modified: Tue, 24 Feb 2026 23:14:33 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json
