## `clojure:temurin-23-tools-deps-1.12.0.1517`

```console
$ docker pull clojure@sha256:31947cda18b368d3fe2ef81a2dc024a9f561a3f7d1fb2e9a8b084dcd03a3f0fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1517` - linux; amd64

```console
$ docker pull clojure@sha256:60996aa37014c3642c900464e497137bc9f922ac0935039f07d9ad4192293ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294791512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bbe7f64d9728905e4aedb95aba97dd9940643f7dea4a0619c36a4b78fe29bc6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a256a356c0c3eb289dc080358c9579a26e9aa5eeea0bab49e560c26b7ea3352`  
		Last Modified: Thu, 20 Feb 2025 02:31:31 GMT  
		Size: 165.3 MB (165316229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23b2705918266d87d908883deff13932ac71c6d8a9ebb3f83476c859cf4e489`  
		Last Modified: Thu, 20 Feb 2025 02:31:31 GMT  
		Size: 81.0 MB (80994555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29faa918c920214a1745acb9c9c7f98d8b814206fafd82d04d15ab98ef9012aa`  
		Last Modified: Thu, 20 Feb 2025 02:31:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3f250f017e580b52466774f08d38c240023470577784d5ae73f4374b26ba43`  
		Last Modified: Thu, 20 Feb 2025 02:31:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1517` - unknown; unknown

```console
$ docker pull clojure@sha256:5f9173cd2092db1cd8b373bb8dd3284d7512ad2c19d07548902d47ddfd086055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3144104960ead914b3bca379a975ecda850ac19aabb8bbeb271a006c6fa5298c`

```dockerfile
```

-	Layers:
	-	`sha256:8e14c5ece95e12882fc0869d34940ceb28d69f9e8585cbf0b920b257ae10bb62`  
		Last Modified: Thu, 20 Feb 2025 04:37:46 GMT  
		Size: 7.2 MB (7176767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f5dfb36e1c5fb422840c0155f98fa1df22d74c607e13869b269f5810e81dd98`  
		Last Modified: Thu, 20 Feb 2025 04:37:47 GMT  
		Size: 16.5 KB (16504 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1517` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5865a198d0f6badf56a9a55836ac6e54f0a1a41c03dbe76754f18c232f3c605b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292493317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1492bd3a9990dd2b458bd0a8441494392901d887cf1bee6547ea110345e28821`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 04:37:12 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca50648c20ef7fd0a5ed1545a1006f88f616c5a3affb90331185a9a998f1dce`  
		Last Modified: Fri, 07 Feb 2025 07:02:43 GMT  
		Size: 163.3 MB (163341440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cffe8cde004092a2753d36dd9d001cf3c1c6aec8449147a42684ed195d3b8b`  
		Last Modified: Thu, 20 Feb 2025 04:01:07 GMT  
		Size: 80.8 MB (80844285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e9de1220290c529ba404cd6797fc3af10ae262e23b49a5ee7de0147f9ff9fc`  
		Last Modified: Thu, 20 Feb 2025 04:00:55 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf72135009559319df3db97e4eedbaba11338eae33218cfba824cf01ad5bcda5`  
		Last Modified: Thu, 20 Feb 2025 04:00:57 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1517` - unknown; unknown

```console
$ docker pull clojure@sha256:20e24d5a0b08d2351e6d8830fc4fbf41f12c522755122109c40f58b60d8eeb6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7198579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12332d93392e9fed6851fee57c679d3c5ccfbf0d15498d2c6a1aade472aad5a`

```dockerfile
```

-	Layers:
	-	`sha256:4409c998b40bacc3d64a76b9586204beb6cdf370e9afd86420d26372702753ac`  
		Last Modified: Thu, 20 Feb 2025 04:37:50 GMT  
		Size: 7.2 MB (7181933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37c50f7ee75c2229a41931abc02a7378d3f1b1d6315f84c2b81a721e7fdba7ca`  
		Last Modified: Thu, 20 Feb 2025 04:37:51 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json
