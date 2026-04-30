## `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm`

```console
$ docker pull clojure@sha256:40264862a97373f4c85ed9ec581600328e88ef87f8cca331a36c4a5ce6468a53
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

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:887646b2b797096405dd03b69b2abb9183ffedbda2352a52b59ce6b190ac85ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275541867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f5fa6d5f4117af1602a4f0620b86ba1f512d15282c02ec48ff0e64c5d37ac3`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 29 Apr 2026 23:15:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:15:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:15:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:15:03 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 29 Apr 2026 23:15:03 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:15:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Apr 2026 23:15:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Apr 2026 23:15:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271df3ff880503ce507a915d37ff4afdfb24397e78a3467fd14e596e32975b80`  
		Last Modified: Wed, 29 Apr 2026 23:15:45 GMT  
		Size: 145.9 MB (145886253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785e47332f73814f96294e6fc85ca3b76681893214a2b515cd3a1fd926c5961e`  
		Last Modified: Wed, 29 Apr 2026 23:15:43 GMT  
		Size: 81.2 MB (81166341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde9be4a71d2411b21b1b3271dee9deb2b20c0ba9d43f0cd6c14a3736c40a9fd`  
		Last Modified: Wed, 29 Apr 2026 23:15:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7c0faf74b9442f8d48e2b31211518476b9610adb6aaef7d91f4c46fd3cf18b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7412654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414619e12eef4a656f2b668ccf15e4b2e9ca51cddaf4a733125b759150e640e3`

```dockerfile
```

-	Layers:
	-	`sha256:b90c76aae4949f6c7b63635eb166cccfc2b3dcb1d56120565dba6b98d7c7d948`  
		Last Modified: Wed, 29 Apr 2026 23:15:38 GMT  
		Size: 7.4 MB (7398445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e345eeeea1bed07722628d7e0f74d50cee1e275bf0e65ea59b1a5ae441b4f9a`  
		Last Modified: Wed, 29 Apr 2026 23:15:37 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:03e478633d8ffd251d9b02ece18c19e96d2f8ce6f7a11914eaf482a1ee1079e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.1 MB (272131819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6157239356229ed9ac33843c0890114108f20f366804bf8f52329747d1d67be9`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 29 Apr 2026 23:14:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:14:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:14:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:14:24 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 29 Apr 2026 23:14:24 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:14:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Apr 2026 23:14:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Apr 2026 23:14:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4b49e403f442e90d4a251f29bb9e9a61012aaa55f4859065fd89d9052797f4`  
		Last Modified: Wed, 29 Apr 2026 23:15:05 GMT  
		Size: 142.6 MB (142583979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f93fd84d8b8d3dd64c99ef319b5a5732092ddeb1382333ac72b1e07b55e79f5`  
		Last Modified: Wed, 29 Apr 2026 23:15:04 GMT  
		Size: 81.2 MB (81174125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709a7751462fb0a2a2be40ca5349dab2f3c35feaecc14d7f59843db08e93ad99`  
		Last Modified: Wed, 29 Apr 2026 23:15:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d61b10e46afb335963c4f0ba2334f769d5d1bf21269329640dbf31cccf45098f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6353265300502c115bb6f5f1b38ffc2899dbcecd6b310ab1cddc603093841cb4`

```dockerfile
```

-	Layers:
	-	`sha256:0f402676992015bc15833005a1299f9d77012de5889f235ca27315e56df9340b`  
		Last Modified: Wed, 29 Apr 2026 23:15:00 GMT  
		Size: 7.4 MB (7404826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:478ad6bb19f300d37edeb0acfd2a6014861b4998ab62e40a78b4602e1ed6835f`  
		Last Modified: Wed, 29 Apr 2026 23:15:00 GMT  
		Size: 14.3 KB (14326 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:ee19ad124fa558689f033a9e1dcc9b7fe3833842dc903b5c4414bd78860e8238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272451288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2e7a0ffa178e30c739847dd90f043e4503cb02cbc307374886c8365c72c057`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Wed, 29 Apr 2026 23:23:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:23:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:23:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:23:09 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 29 Apr 2026 23:23:10 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:29:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Apr 2026 23:29:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Apr 2026 23:29:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237ef4f7556b579838f856974008ca10a74407a11bb8a3d8ee66e54d2f440d6d`  
		Last Modified: Wed, 29 Apr 2026 23:24:49 GMT  
		Size: 133.1 MB (133109625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9259bad682db6e45b6440691c55d68916c1f0224661e42bbd391121396840a4`  
		Last Modified: Wed, 29 Apr 2026 23:30:18 GMT  
		Size: 87.0 MB (87004283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767a3dc0a295bd7d28ff25c8307aad812b3738e13b1e78aa0f3eed8ba6e23d2e`  
		Last Modified: Wed, 29 Apr 2026 23:30:15 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:48035310cbf52f5c9a2a306052c5f50e78d18392ff934000863cd45904058005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7417303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea49af942484c98a43661adde26d0b8e2c031f1615598f5eed9b041e2768080`

```dockerfile
```

-	Layers:
	-	`sha256:a185c315b6f09b42a9c686f15f01f7bfc41167a94e4462ab42c51784988afa30`  
		Last Modified: Wed, 29 Apr 2026 23:30:15 GMT  
		Size: 7.4 MB (7403046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6bc6ebba741e0b07c047e7709c29cabe874b99e91ad1f1a867d542fb2a60a77`  
		Last Modified: Wed, 29 Apr 2026 23:30:15 GMT  
		Size: 14.3 KB (14257 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:7ddb6f07fe0b77a262cd1fb8f22290cbf8db7de4751139ed1e223b6268d3b322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253781172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af0e700f74691b815b342eaebfbb427b7c704b7f05be12652e3b3ec2d88fc904`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 29 Apr 2026 23:12:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:12:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:12:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:12:54 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 29 Apr 2026 23:12:54 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:14:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Apr 2026 23:14:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Apr 2026 23:14:37 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9877cfa317cb3a147f3af298dc6f97e96426f3a35ab1d50968ae58d675a805f9`  
		Last Modified: Wed, 29 Apr 2026 23:13:35 GMT  
		Size: 126.7 MB (126652695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a80cc25dba2d73816d107005dd02248bbef7e6dca0678b6d4d07fc1ea2cc70`  
		Last Modified: Wed, 29 Apr 2026 23:15:02 GMT  
		Size: 80.0 MB (79979863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071d09ba97e0f5b47722d7f2dd5989084fa9404dc6013a5b97d30754a640e8a2`  
		Last Modified: Wed, 29 Apr 2026 23:15:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:014e3c0bdd12d4ca9cfaa6c96b144e76cd520820404dc58f7197fa19e64317dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3967faaa5bf9da6bf52cf6b74c472099dee79a12b89910987706f1d2d70a78ea`

```dockerfile
```

-	Layers:
	-	`sha256:67f548dbb9c8004ae628ac561d8f6fc201ba87c65a60c4a079cec8d2440ce6ea`  
		Last Modified: Wed, 29 Apr 2026 23:15:00 GMT  
		Size: 7.4 MB (7389768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2cbee656bdac5e14814e6f6ca5767fa43be4cbb6fc83e9ff0f1cf1af9d18d83`  
		Last Modified: Wed, 29 Apr 2026 23:15:00 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json
