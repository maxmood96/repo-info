## `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye`

```console
$ docker pull clojure@sha256:3d8bb753f1a32517a2dec40c2becbe5e0038a4cc59585ecd2ec58712e0919612
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:14d84e4d984148e6e41c782ea3d90800cd6819e951263a777f3952d9f2ff72a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268778153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c9ab4bba702a5209b0f1301c5da8c02543e964dd90361853819cf7f5981e85`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1129f5a88aab2573b6f924e429ed0a9d975e6438ddf3ff9813952b0b450d4b63`  
		Last Modified: Mon, 28 Apr 2025 22:06:57 GMT  
		Size: 145.6 MB (145635848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05add4e5f3735b4b95fbdad491d83abb30c0080b5a6e398c906b1af4df0386e8`  
		Last Modified: Mon, 28 Apr 2025 22:06:56 GMT  
		Size: 69.4 MB (69393922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ab1427222dfb58935ff50bf704e8765a3aff7dc65d536157283e67a8e72ee9`  
		Last Modified: Mon, 28 Apr 2025 22:06:55 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3467c62fa939fce2d78b3238534592efb3a1e6d0918a7df8c9ba460e6b8646b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7240948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d82a15cd5d60a11b3c256d73935f803246f943decd99dc2fd5a2d00d13e014f8`

```dockerfile
```

-	Layers:
	-	`sha256:1b648c77bc6c3a947a188ddf834cfe61a2d1272fe07456c0b81bbba6148ea1b1`  
		Last Modified: Mon, 28 Apr 2025 22:06:55 GMT  
		Size: 7.2 MB (7226696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc76e6ebe59184abc22dbb3865e4bca4cd426f8a6e8268b8e2d2d41bfa830aff`  
		Last Modified: Mon, 28 Apr 2025 22:06:55 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1a2ad3ce6e180aac6a93bb57e7a9c23a0c9ebaea36716cda4ce24fe4d59f619a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.2 MB (264206154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:051759ab1397979c2568181d893fb03b03697a73cd19578f215829d1c928f788`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6547976fd91789f51bff85ffd649e7a0f8f7fc9fdd76aef7c938698e4a3ae156`  
		Last Modified: Wed, 23 Apr 2025 19:37:50 GMT  
		Size: 142.4 MB (142422063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61f3f0a012780c00bc2e9b4a37c89aca2ef54d4b9d68eec4bcda0d33455012c`  
		Last Modified: Wed, 23 Apr 2025 19:42:31 GMT  
		Size: 69.5 MB (69529222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad41899cae85ad5843092b603d0c689ca908ee72964d163551fcc15bdc6c07fd`  
		Last Modified: Wed, 23 Apr 2025 19:42:29 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:56802199480bcdd444c1949e0b3a878ce65ff95189e86f3a1a38dc7a7015b7d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7246729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb008b5a313dbbcbdd24361533ed25b39cab1366343ec596a323d91c7facf79`

```dockerfile
```

-	Layers:
	-	`sha256:a93dcc2362bc038311bb236a65a1433748eef2b123256bcf1c0d30fd413d4726`  
		Last Modified: Wed, 23 Apr 2025 19:42:29 GMT  
		Size: 7.2 MB (7232359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:336f0b02f51dfeef8c66580a31e70d5910f8ecef2df2067c452c040da27ac682`  
		Last Modified: Wed, 23 Apr 2025 19:42:29 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
