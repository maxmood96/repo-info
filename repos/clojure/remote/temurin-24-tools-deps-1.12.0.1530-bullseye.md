## `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye`

```console
$ docker pull clojure@sha256:5b9147b2493aa3454b9cd253d85daacbc04d22ee369b674cfe0a98fa0e6e12d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:4ef64b35097de6babfc2ee4254d157b024d80422d51db9de42d9b92505d7b553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.1 MB (213101955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8691a6c4ca1a6000f076a61c99eab755098b3ed67869aee5ae334624a05a475e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671b36b118546778f621aff30aa94605755a96eff7bffba6067cd81b207581fd`  
		Last Modified: Wed, 21 May 2025 23:34:53 GMT  
		Size: 90.0 MB (89952021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6713e04a05b4abf38dd52c0e7591ab38b1a0505cf8180be360def39529acd769`  
		Last Modified: Wed, 21 May 2025 23:34:53 GMT  
		Size: 69.4 MB (69398700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5a848b3b1514df49c809a565bbb6d673cfa737c286752c7d3697eff7eb583a`  
		Last Modified: Wed, 21 May 2025 23:34:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16736939811007dc3142502f48ff80ddb308aa98060cedc5c0fbe235af5ce71`  
		Last Modified: Wed, 21 May 2025 23:34:50 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7cba900626778ffcfc5b164f9e06271be70c6c0d76fb0cd5fe421ef4cfb5fc81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7221050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc2fe3caf6e40abd7fa1a17567c66b70dbfc3674252c7c7e9a09786a4615bd8`

```dockerfile
```

-	Layers:
	-	`sha256:418ff3b21047cc3c8fb3fb43557967c6f085c89a783628e29e61b6c4fb61f490`  
		Last Modified: Wed, 21 May 2025 23:34:51 GMT  
		Size: 7.2 MB (7205236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fd980aad97cc96b63f5a476d406598e686715b0e24e6b74a597f29158d6c682`  
		Last Modified: Wed, 21 May 2025 23:34:50 GMT  
		Size: 15.8 KB (15814 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7d5068ccb5ee1d57be31d7efde327516b6a127965f47c4836abbf53c4c467fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210870633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f3bf0a55daef4ada020a0742774ecbc919a26a86caed5000d67723af1cb359`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Wed, 21 May 2025 22:28:12 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4d6f57ce17d9b1e545949e47ffb51eaaf6c23a96fe74a72056817227fcab22`  
		Last Modified: Thu, 22 May 2025 08:40:27 GMT  
		Size: 89.1 MB (89091270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b750cdf9d6a9b431dafb25a25f6b93f903a23621c6981172e751fdbeaecb5e64`  
		Last Modified: Thu, 22 May 2025 08:45:25 GMT  
		Size: 69.5 MB (69530568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15b9792c5a80a2e5a9583213132dd3ac7e463f9d1ab319900db46c6ddad17dd`  
		Last Modified: Thu, 22 May 2025 08:45:22 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e3b03b288cdd376eb7c3562ab7b112a3c00b087a0836ac18497900d0cabd65`  
		Last Modified: Thu, 22 May 2025 08:45:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b2d1a05cb24fc2be87ab31ce1edc5ee22e94a35725f9b70bc11a29e3c52d0036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7226263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7e61dfb6458f163a75318c42ec3fb3378b76bc34c290e78cf2cd9df6ac9d3a`

```dockerfile
```

-	Layers:
	-	`sha256:fc4e362e5178ed29edfedde90b5d4c2c3fe06e8d51f7b5f33095a5bf488823f5`  
		Last Modified: Thu, 22 May 2025 08:45:23 GMT  
		Size: 7.2 MB (7210332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0aaa53533dfb4160ae792ab371d95f8be333de051f961d2429b28dddc2142a8`  
		Last Modified: Thu, 22 May 2025 08:45:22 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json
