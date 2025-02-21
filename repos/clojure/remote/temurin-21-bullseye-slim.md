## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:0da9e8b6cae054ef33e1c1ff70030e8955942ed4234fe504848a851faaa963d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6203053e6e23df2ef008d1de02f0df45ca2c85287d942bc3fc15bff21f0c5e91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246627870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f5e340de15cee952435ad26cce9df618fbb87ed044d0cea388cd9ad00b3686`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab077ee19448111472bc20c6ab915e7fdef319f38ca8a821088242dd0273e47`  
		Last Modified: Thu, 20 Feb 2025 02:31:14 GMT  
		Size: 157.6 MB (157585894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a000a5ad4b47c282e11a74353becddea1f69a87364fa62ceba87295054335b9`  
		Last Modified: Thu, 20 Feb 2025 02:31:12 GMT  
		Size: 58.8 MB (58788346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6d1e171f0a752f33f6a8679dfb77603bf7e21ef26934002cb15a4c20c42095`  
		Last Modified: Thu, 20 Feb 2025 02:31:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89560a1d64ddd70377f7cbc35837a22b95048ed52cda8b135beaf5bab971dc03`  
		Last Modified: Thu, 20 Feb 2025 02:31:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bf6be97f8da99d5a1222de84201aacdf7cbaf9dd677699fe3a7b41a08ca024bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9eb75e6064130bf698314df6a73a547c97602b0f7451b4c179f4e303ee0535a`

```dockerfile
```

-	Layers:
	-	`sha256:7350b33be2cfa2d10db02a1b65d3c601671f6d497db4631493c09a17c8235a3a`  
		Last Modified: Thu, 20 Feb 2025 02:31:10 GMT  
		Size: 5.1 MB (5120865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f181abe7115f22dd9be549cb1e33178e6a0575adb353300025f6d6feb77f990`  
		Last Modified: Thu, 20 Feb 2025 02:31:10 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d130db3139739f8deafaa38c320b7104eeb2ba3f1a176b5ef2e622afce5a9e0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243515490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7207822688a02071d8e5b153243f114068f224344495812b445a9e08f59edbac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 01:38:25 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1444b3218878a3b35e8951a2bc0e44515e7eeec8e85c72e00762e9498d1e33`  
		Last Modified: Tue, 04 Feb 2025 23:54:01 GMT  
		Size: 155.9 MB (155859274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f2ca8bd76b238d052a2de2801a16ff709a5a9dc5d2c07f0ff73802163c49ee`  
		Last Modified: Thu, 20 Feb 2025 03:58:26 GMT  
		Size: 58.9 MB (58910365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc47b6bca9b9fb9b78694081aef7fa088ca4435c56d6935510c4d934981983d`  
		Last Modified: Thu, 20 Feb 2025 03:58:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4d53ef99e12c49789e6a376526873a5cdc5224ae18f4a243560080a3fc63f0`  
		Last Modified: Thu, 20 Feb 2025 03:58:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f80de46f8e68f01673dcbde06f0b35f95eb23b9eed1d856b006fa34283b8f975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5143338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:705b9d8c6998f097dc30ec64f81ba9b74c558504611edc7d2bf33aff28be0e28`

```dockerfile
```

-	Layers:
	-	`sha256:91c743471467981ac9492370907148329fdc310434588b6eb4e346baea891cc7`  
		Last Modified: Thu, 20 Feb 2025 03:58:24 GMT  
		Size: 5.1 MB (5126621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a65186017cb23ae996c59d1230209afcce01cbc78b172fb7d5dc5b93116d3dff`  
		Last Modified: Thu, 20 Feb 2025 03:58:24 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
