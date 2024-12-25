## `clojure:temurin-23-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:617b9bfd03cde38dbbe619e5f3eb507807cabfb6bc4b1ed8635b6aaa4b9eac6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cc46462067d4740730dc91208f9289f8a84dd962f592afb0edbedf8d012998d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254304959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a2776bbfa5b9d06bdab9d1d3d8ee1d8b6fe4a8bd0662c3ad6d6e5dac0b2a5f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ed10d0647783c33ead6a3ebda02b1e5bfebadafc4da9ca50b866c2c4635bbc`  
		Last Modified: Tue, 24 Dec 2024 22:39:23 GMT  
		Size: 165.3 MB (165295092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bc1995721921f774e14f1acdb846e02771819c38e8f2078afeb6c8e565ca1a`  
		Last Modified: Tue, 24 Dec 2024 22:39:21 GMT  
		Size: 58.8 MB (58756181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fe46dd2e4bdbb1a4c457f37c475a362356923662548af20614108c278c987e`  
		Last Modified: Tue, 24 Dec 2024 22:39:20 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2cee38f6f8b14862819fef59ca9e705103ec84f9370d812b6adbaa95cb3af4`  
		Last Modified: Tue, 24 Dec 2024 22:39:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c461f1c8eb8164724736fe09dcee61306ced6cfe4e2423966e2073bcbf418c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a2349601ec967927a37b119637f3112bd01ca2b88b36e7b4573c3673597b99`

```dockerfile
```

-	Layers:
	-	`sha256:4c3542db63608bf2f12bf37ff845b16bfe8c94b89d3b4c94192e725a40814484`  
		Last Modified: Tue, 24 Dec 2024 22:39:20 GMT  
		Size: 5.1 MB (5122012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6b1d4db5a94a52a4ffa072abce45749b32bc568f92c10055c129cdb08b8a49f`  
		Last Modified: Tue, 24 Dec 2024 22:39:19 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:758d1d5ee254e65d4d47bd4b17a69d242adcbd4b1515ff3b76d16061c1146413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 MB (250908022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:464fd2743cd44fa3d30310cdabe341281b6435acb82ed5aca681c0494cb645f4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c788e772ea911990d57e5f952f630757d6bd8d9e9c0bb82ec7e6021b67421c9b`  
		Last Modified: Tue, 03 Dec 2024 15:35:01 GMT  
		Size: 163.3 MB (163281795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986afaa046f7de85b2eaff4c728a7ffefc2ba4bdeb616c724c53577ab847d393`  
		Last Modified: Tue, 03 Dec 2024 15:38:53 GMT  
		Size: 58.9 MB (58880265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec06574d02689990734633b76bcc27ca744884345eb171a2f739736d6d9f19`  
		Last Modified: Tue, 03 Dec 2024 15:38:51 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbb2da8bac18c29144a886c23037351aaca98a3cb194b3f298cfa0e08285734`  
		Last Modified: Tue, 03 Dec 2024 15:38:51 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6a330d7fc915eb7a8602145beb344e0f4128dc079c48f53c6522ca49b6bc4c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5149673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0238cb69037e22bfd3d1bedad5015cddf4792dcf8d5b4aeac670056c771ca0b1`

```dockerfile
```

-	Layers:
	-	`sha256:a783360852cf9fef3a8bed473545dd7bb7c0fb247e6c8aaaa31fa2d4ca9b056d`  
		Last Modified: Tue, 03 Dec 2024 15:38:51 GMT  
		Size: 5.1 MB (5133677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:289bf231e4e1de9ebe23bae37403ee3ef89db62a68d4e31bc2bca6aa54e0bb93`  
		Last Modified: Tue, 03 Dec 2024 15:38:50 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
