## `clojure:temurin-8-trixie-slim`

```console
$ docker pull clojure@sha256:fdec426e9129fd89e80c3cf9f0808ec85d85399ce61395a00617a3baa8ba5412
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2f48be305b9ae4ab38777268e94ce329b0a5f37bfd3e03d29d9fe49bfda936bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157025679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7753a5a1c1feb8c15ce031a2f783bde5b4eceaf7f14295d53e1207760e5cc4`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:13:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:13:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:13:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:13:33 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:13:33 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:13:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:13:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:13:50 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6974508e9c6ea6593ac50bc70a7dd382b474bd82c82e35d5a524a3939befbae`  
		Last Modified: Fri, 15 May 2026 20:14:07 GMT  
		Size: 55.2 MB (55198707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02e3fa0d1b9a76e41e55a3442202a4371854e551e64d525bca22ad2e2479af6`  
		Last Modified: Fri, 15 May 2026 20:14:08 GMT  
		Size: 72.0 MB (72046100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd6355056f03f784e7b497fc966a12d130c5970fc396ebdce91537be47197c5`  
		Last Modified: Fri, 15 May 2026 20:14:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c45d078dfd875ac4b434d8baf8a857672db109d396e7db56aaf29377f3ff3c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5394595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3591755a1bdb6b526ee2aa3177b8e6298b022cf412c4bc7c267d4a7c8a5a31c`

```dockerfile
```

-	Layers:
	-	`sha256:1c86a23bf67401ca7808935f7604ad895bb1bee5d50be2a38c6e9843ad550bfc`  
		Last Modified: Fri, 15 May 2026 20:14:05 GMT  
		Size: 5.4 MB (5380213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73f9c2f1aec20927a00cef08f361e028f7c9e27acdde499c5aea5ae0292919f6`  
		Last Modified: Fri, 15 May 2026 20:14:05 GMT  
		Size: 14.4 KB (14382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e3cc5d04f0892b1452586fbbaaea455d09314580b941062631b238ce7c1a5f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156272020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e815aaa57fe1f0c5fa0c3e01d3060f19fdf6f6ec66fb5473994ecf88a3110a35`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:13:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:13:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:13:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:13:39 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:13:39 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:13:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:13:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:13:57 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417e2bcfec3ffafbbeb36418a3b7d03c4cf763c50b8d8bf8c8a18595fe115803`  
		Last Modified: Fri, 15 May 2026 20:14:14 GMT  
		Size: 54.3 MB (54272935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4911d22e12c8fddcae32143ce60da1bb3ede0f04cd31fc894c150de2b4027ecb`  
		Last Modified: Fri, 15 May 2026 20:14:15 GMT  
		Size: 71.9 MB (71854797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d0532e2392378b142a039dfb8ae95950d60e91fe0df449ea9c84670ca86e30`  
		Last Modified: Fri, 15 May 2026 20:14:12 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:16fc7828c54ca60d6a086e1e77dcf5b7c55648ad6ae0d2e57ee2b7eb4664e24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5401182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbed3ae94ced2488993ec3a25b068c6092296c6f56f2c46f3467691d3e4f5443`

```dockerfile
```

-	Layers:
	-	`sha256:8b69a7ed52ef118e97a5be165c2cbbfdaf14212af2d3c9a373e774c21fb7a010`  
		Last Modified: Fri, 15 May 2026 20:14:13 GMT  
		Size: 5.4 MB (5386682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db1657ab052d26c7b266f6dec7dbb08813bd02d6cf1e053d73bb797e26ca6d6c`  
		Last Modified: Fri, 15 May 2026 20:14:12 GMT  
		Size: 14.5 KB (14500 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:cb436a1711a40d8908cdf5849a94f7f54fc193a33ef3e131dc09ef27c3606099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163724454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e879741a687c80fe2e60c676a788dab7151c7643c7881f8aa2c1511b344f74c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Tue, 12 May 2026 21:49:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:49:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:49:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:49:10 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 12 May 2026 21:49:11 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:17:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:17:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:17:47 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6108e5c2a2245ec0c51d22b23687faec2598356811a7675057929aac5f8deda`  
		Last Modified: Tue, 12 May 2026 21:50:14 GMT  
		Size: 52.7 MB (52669152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909f341bd605d5ae237f974afc0b5e84f1a8365aff56f6a92abb41b8c29f37d1`  
		Last Modified: Fri, 15 May 2026 20:18:26 GMT  
		Size: 77.5 MB (77456569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639a024378aa5857d0709ba9a019824b7f62c0ec88cabc150fc75e19eda047d6`  
		Last Modified: Fri, 15 May 2026 20:18:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4f3d4e93d4ad08e797f9b27e2bceadd5ffb37c08e60903e8ce472d4a66ff9c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5399609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0841fbd6ae488fc6a62896e59febbb0876d588776cd841e767223d7686b85395`

```dockerfile
```

-	Layers:
	-	`sha256:7885d99b972e7c9d2295a8236daf89c568df26495d344516184a26bdc9a1a0d3`  
		Last Modified: Fri, 15 May 2026 20:18:24 GMT  
		Size: 5.4 MB (5385179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:971484feee30b14fdbb24eebda0d1a1c3762f091b344352f2418a2b232ed6d4e`  
		Last Modified: Fri, 15 May 2026 20:18:23 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json
