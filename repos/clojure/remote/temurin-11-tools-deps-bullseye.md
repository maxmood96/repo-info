## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:2e0144cd6f634534ff9e44534845b16d315811af636478035cfd1f24f1164e63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:2aead5489dd05aa9e2b4836afc9cff8d2480af84895848d156fc80a5f9578310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268519631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b4518094aae1e01f9a1d52f70606c61f99eedfdd753ff78a4b4aa7a84652bcd`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030b19a1def526ce102fd9bf80b1804a4bdfa2bafa721151475c07907444fda4`  
		Last Modified: Tue, 07 Jan 2025 02:29:37 GMT  
		Size: 145.6 MB (145601480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d8ae6bd2fc3de43a6cfa6035800451c6999f9838bdfbbfce3f190d5012d535`  
		Last Modified: Tue, 07 Jan 2025 02:29:33 GMT  
		Size: 69.2 MB (69178549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6240d0775ef20f3fe07d392f9b7c06fe5e0395bd59e08c088448efcc34c04c94`  
		Last Modified: Tue, 07 Jan 2025 02:29:31 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6b284bfabcecab9a06275947713dd6dcb1ab16ffa7c8eb7c83f7df4e5ddd17d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7238948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9804d3bcb90239f57cba6ee1ae88a6cdbb61ea856ee9edb2fb7a3bcb932ea2`

```dockerfile
```

-	Layers:
	-	`sha256:92df9fa3615a51dd1cf2593f0b3ce0dff239f7df1ba4f6c3273646c74f8a76b1`  
		Last Modified: Tue, 07 Jan 2025 02:29:31 GMT  
		Size: 7.2 MB (7224696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:154945c0eae3c18cdddfe27ca3cd83692d7a2ea429f060238bb050a1996d85c0`  
		Last Modified: Tue, 07 Jan 2025 02:29:31 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2f4b3c7bd9d22f58be0ea136c9c294d16dbd2f9f32b3ee9a90a891f7f401b45c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263939832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c2a583f3ce4c02944d88d531198edeccbaf715df40f26cd0f9be74badef894b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac580959112f2958e7f4b4eb9b360444b899d195029d8e7b71a031c4435f09e7`  
		Last Modified: Wed, 25 Dec 2024 07:20:01 GMT  
		Size: 142.4 MB (142388995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f5ee8ab382c77050510270f5323af29de034ac17e56458a3380c4ccdfa7ff2`  
		Last Modified: Tue, 07 Jan 2025 03:24:02 GMT  
		Size: 69.3 MB (69304495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0165a15c3df5d3bd14b0069b8f5d54c9acdf6f3b7ea91e6667db162877653881`  
		Last Modified: Tue, 07 Jan 2025 03:23:59 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:dda5df30d5e29245cbeceb07ffe957c6fbd84c6cdd5bfdb385bfef3490d03fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7244783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e68180484a80a1ca8a81ea8314eaa51a5bc9f028d3f6f948b28c8d5ffa1a54`

```dockerfile
```

-	Layers:
	-	`sha256:5e52153ccdcd72625e23f3f5b0a3c6ce3475d960dcc9062b2760150d1fe2c46d`  
		Last Modified: Tue, 07 Jan 2025 03:24:00 GMT  
		Size: 7.2 MB (7230413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bbfbd15cc3eda14cc6a74fb6bbc5ded0fb26d6c050d447ac1e7f244776f3cc5`  
		Last Modified: Tue, 07 Jan 2025 03:23:59 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
