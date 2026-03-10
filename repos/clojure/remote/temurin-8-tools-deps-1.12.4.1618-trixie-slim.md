## `clojure:temurin-8-tools-deps-1.12.4.1618-trixie-slim`

```console
$ docker pull clojure@sha256:e241e0a721842864b8d4432abfdced1a4582e55f82e780a21d68b5cf79f223aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1618-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f90a7c7be08a279d3de4e1ef984b1ec6f0dcb17fdfab0c620301a0490b70b19f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (156964211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87da853566195a3253e7c0cd09286074d95659325077691a9c7b14003913626a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:33:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:33:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:33:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:33:51 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:33:51 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:34:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:34:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:34:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce4b7eece1d3b8d12bb9c4b278cc631aeef8ccc7e50ef708657a84b82497404`  
		Last Modified: Mon, 09 Mar 2026 20:34:24 GMT  
		Size: 55.2 MB (55170047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a96a7b01ae6800246336a052a455cbb00aca36f113145e491003108c199cebe`  
		Last Modified: Mon, 09 Mar 2026 20:34:24 GMT  
		Size: 72.0 MB (72014886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7e3c4b44c518796e94bcb4042898dedca5a244575bb5c6fcb85390fe2cd365`  
		Last Modified: Mon, 09 Mar 2026 20:34:21 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:63b77ce2c2e6a98ca07580b4cd090767e8f521a2749715febdb63e7cc23770f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5394279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8e81d862de999f05f00731e53b8d1677fed296260f120de98ee181ec480558`

```dockerfile
```

-	Layers:
	-	`sha256:d72641f71736ffd972556445e88db0901fd013c0abb1b14407783a3438f7b05c`  
		Last Modified: Mon, 09 Mar 2026 20:34:21 GMT  
		Size: 5.4 MB (5380051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:122993c9ce68458ef375df95dc6bb3e0d51e87ee72c99d5ef818e803e777f928`  
		Last Modified: Mon, 09 Mar 2026 20:34:21 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1618-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:47f0be3f8a3194a4d11017c0004921079f30073c13d2828a3c0004c2d200127f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156224527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd2de307d7d4e633441c7de913ded8084eb2bfa3d3fb9af45277fc4877e3dd3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:34:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:34:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:34:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:34:05 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:34:05 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:34:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:34:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:34:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dcad01b19bcdb8cfb3ebb9e2424fcc4c4d5e871050ceebc7ed3f0f0441cff05`  
		Last Modified: Mon, 09 Mar 2026 20:34:41 GMT  
		Size: 54.3 MB (54251616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca391c8f6597c85f2f4b527c105918990822de6b0e37193b9ab1a557e18d5e0`  
		Last Modified: Mon, 09 Mar 2026 20:34:42 GMT  
		Size: 71.8 MB (71832167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce44381991735e1dde5fa415a52c175e97712ac79edc9aff5d62d64139076c6`  
		Last Modified: Mon, 09 Mar 2026 20:34:39 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:96fb81318b4705d49d82bdf860fe95f8cb96c9da2918fb3444690476d68c75a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5400866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14189c331833254e19ca9e39f94a2da6b184fb489d97af2899530ae737de183`

```dockerfile
```

-	Layers:
	-	`sha256:fc949e8b3070e9c1b8f8ff417c2190277e6a896c4888ec8c6a578ac14415b531`  
		Last Modified: Mon, 09 Mar 2026 20:34:39 GMT  
		Size: 5.4 MB (5386520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2e1980ef762c10d0e1d3639c8a618d809f85dfb9118c779a7e73d3aed14b8b4`  
		Last Modified: Mon, 09 Mar 2026 20:34:39 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1618-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:689f18c9972b6d8287c0d185f5ea3a5b3750d6744bc325ddcd2daf7cb11d2a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163679961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b40b95a48b0b13dd124af307ebcf05486ccbae6c352cd0a614fea45275c750`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:44:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:44:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:44:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:44:31 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:44:32 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:45:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:45:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:45:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47c419cd8945a2a23367ef4a3e257407fc2a7d4756b1ecbefb7b72be5b993e7`  
		Last Modified: Mon, 09 Mar 2026 20:45:53 GMT  
		Size: 52.7 MB (52650417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1edcf0df58b674a45f9749ac448dff4d7a0d5c56ba314b41affde1b713b21396`  
		Last Modified: Mon, 09 Mar 2026 20:45:54 GMT  
		Size: 77.4 MB (77428683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584f610d883d70596a112090ff75a5d0cffc8c802e74866e2606fe3bf73d23a9`  
		Last Modified: Mon, 09 Mar 2026 20:45:50 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:99d7b432bf0779ec2153ee4abfa23e14811d2a456cd63b83ae2ea217f0a168a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5399292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680f1fcf84a6bc24cb54c7b22cec54bdffb9614eaa96fd9d387cc88d9bc696e1`

```dockerfile
```

-	Layers:
	-	`sha256:600e2051f9090c4696adf5ebaf5b317a71c0c165d6d4b5c98521663f9290896a`  
		Last Modified: Mon, 09 Mar 2026 20:45:51 GMT  
		Size: 5.4 MB (5385017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c816bab74abb85fc9cb25849390fa8999cbf8a99cc611a73c0ea95847518130c`  
		Last Modified: Mon, 09 Mar 2026 20:45:50 GMT  
		Size: 14.3 KB (14275 bytes)  
		MIME: application/vnd.in-toto+json
