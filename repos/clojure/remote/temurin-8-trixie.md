## `clojure:temurin-8-trixie`

```console
$ docker pull clojure@sha256:731328e6d63632bffd3f99ecf86f5064764ef4a64d20aa85f09659ed12f7bccd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:01b14cea1523849637c83818109c85b3caa78555be47605866ea4a7c1d3a2451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190005684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2159c35d5c5d1e89b4d32cb770417e4ccbedba09bf66d0ec1798b140f922c2`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:01:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:01:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:01:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:01:42 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:01:42 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:01:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:02:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:02:00 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4bacecf22cb768b1b17664133902ed224d43519cb2b59ff68efe2bceb8ea96f`  
		Last Modified: Thu, 05 Feb 2026 23:02:22 GMT  
		Size: 55.2 MB (55170168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1e43ad7232594a072b40f117dff0b97a3d78187a35c14611e424bc7d95338f`  
		Last Modified: Thu, 05 Feb 2026 23:02:23 GMT  
		Size: 85.5 MB (85541920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f0db0fb4f3fd6227d309ac4330b5eab530982f5b93ca949d69e3dfa4219f27`  
		Last Modified: Thu, 05 Feb 2026 23:02:20 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:de4afe2fc98bd1183cb3c592f269933e1a82bb91c464c66daa9f65c2a556eb82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7604237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75e305b2e30625e261d6aeba4dea646d49073bcfda9e825aa0d427d6bb65456`

```dockerfile
```

-	Layers:
	-	`sha256:06c3f0955ad2bf1833961292c091f5a2678b3eb4d510976f3e5483034388f1eb`  
		Last Modified: Thu, 05 Feb 2026 23:02:20 GMT  
		Size: 7.6 MB (7590067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b03ddf685c776af9d04ea786dbf97851c6103e1fdce6fb36e19fa31b92f3ca64`  
		Last Modified: Thu, 05 Feb 2026 23:02:20 GMT  
		Size: 14.2 KB (14170 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ffb64d6e06250f73b9b5637d6fb9a8034ab210461cfc060fb9484026d57440f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189265259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286fbbf7e85bcd489d414142f010134bc703a36eb735852ca54c5380ae8c1e63`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:01:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:01:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:01:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:01:53 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:01:53 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:02:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:02:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:02:57 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0616780b731961cb91ac6c12043aac5f704e2e80d8d2940c74e14e3733ad2d5c`  
		Last Modified: Thu, 05 Feb 2026 23:02:32 GMT  
		Size: 54.3 MB (54251610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d3eb1ed5f3c7306817a47e8bb8350ec0314dcc5c19746b5f1b7c66ede27b62`  
		Last Modified: Thu, 05 Feb 2026 23:03:16 GMT  
		Size: 85.4 MB (85360986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1091cc80be29f589352457a04d86a73ec8bde2a0f4822a601561d93936837108`  
		Last Modified: Thu, 05 Feb 2026 23:03:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2083bf8c894f751453da907ee066935be2228505417e63ce367ab32e680764f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7612084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae09f729a71751bcb295f01423671ad5d874097c214459eac39c195777faba5`

```dockerfile
```

-	Layers:
	-	`sha256:d89266eb93acdbc25b160901d4445e03146571a04bd14147d521397b9fa22e22`  
		Last Modified: Thu, 05 Feb 2026 23:03:14 GMT  
		Size: 7.6 MB (7597797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7b83e3ac48ce9fa229d5f1c26179f2edc04509be7327a6738dcb5b68bd5b215`  
		Last Modified: Thu, 05 Feb 2026 23:03:14 GMT  
		Size: 14.3 KB (14287 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:15f95d7f1b8f11e9be4d106229c1c67943270cb743be8b808f1399e61a751761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196710226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f5eb21aee2d6a7cbe3797c43cb28bb6e983c8492616e403c085714c81586498`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:59:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:59:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:59:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:59:16 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:59:17 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:07:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:07:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:07:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e31da8e0f9e130c166e97ec3b0c716f0ac97a7e8894e13f7961b61b37819485`  
		Last Modified: Fri, 06 Feb 2026 00:01:40 GMT  
		Size: 52.7 MB (52650394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329a4ba3aea40fc559907aed1c8987fe5d99a928d3b0eedfd7b978c4b55dc94e`  
		Last Modified: Fri, 06 Feb 2026 00:08:57 GMT  
		Size: 90.9 MB (90947071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b636d89a0392804a99da1d846f95ac4291d2ae62e0e7425076e2f9a568fbe76f`  
		Last Modified: Fri, 06 Feb 2026 00:08:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:48b92fc3953c8597fc9774bbff268f7ad9946bf3ce7f1c732a9fe41756634837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7609300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d7ccb94ee8bf4435411bbde927fc2dd518b769f65d8151c3eadb66a1c934cbd`

```dockerfile
```

-	Layers:
	-	`sha256:8e2b4a04977b278ae156743c4e2605ec905e780540e1e6e923e7d380c408af34`  
		Last Modified: Fri, 06 Feb 2026 00:08:55 GMT  
		Size: 7.6 MB (7595083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03e991ae055761181776fb38bfcb4b3cbce7017406d9098f0ea86d8b49adb661`  
		Last Modified: Fri, 06 Feb 2026 00:08:55 GMT  
		Size: 14.2 KB (14217 bytes)  
		MIME: application/vnd.in-toto+json
