## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:54583e87c8ab59e1df282679a6cb2506ac35c89b6ce252dbccb0a249761510df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e0b0179db3c5a1e860ce63549af53ab4adc74701bb3649a2e9912f6ff37fd05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268976396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9b4dc02a903668a59badc650cd401b50a639f4703d7f1be58cd3e8ed5d9859`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:54:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:54:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:54:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:54:28 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:54:28 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:54:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:54:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:54:41 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e230eb7a764790ec08bb5869326dd441ea7f0a578b278a6a17d70de19e0e51`  
		Last Modified: Thu, 06 Nov 2025 03:14:02 GMT  
		Size: 145.7 MB (145658319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfe515071436415e3ea630e028c987a99d0586da885c767f692ed1fc261d0f9`  
		Last Modified: Tue, 04 Nov 2025 00:55:14 GMT  
		Size: 69.6 MB (69560740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da121d909a9b77faba757d016d99ea42a89ccce036758e260aa84d2f135f49fd`  
		Last Modified: Tue, 04 Nov 2025 00:55:08 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7c0ee96358caed13024ea2e29784135fd3ab241905a95d68d6b89f2770a218be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eeb32fe3789712116aea49009f10dd64fbfdff28e05a51ef2abf4d9f2d728e5`

```dockerfile
```

-	Layers:
	-	`sha256:3bb1318c7e7d406204daf79383c220f2afcdfc90afe01a56044f3260641b1cf4`  
		Last Modified: Tue, 04 Nov 2025 10:36:25 GMT  
		Size: 7.4 MB (7415808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39fbda3cc84380435c7241de9519f62bb0d1724f40e9f3f790fce7762f1a4d7b`  
		Last Modified: Tue, 04 Nov 2025 10:36:26 GMT  
		Size: 14.2 KB (14207 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bca671ce936f9665d9fef420f7c273c497a2c25500ad86e71ede1760eb552d6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.4 MB (264407370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4529286ac86093e22ef8de8114ddfdea8a13759fe177d2cc2125b1eb1ee06b2`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:54:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:54:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:54:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:54:57 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:54:57 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:55:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:55:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:55:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee30b7aa89d517b9683ca7b51c4f9f4dc80677e6d32c4570244b5e807cf79e6`  
		Last Modified: Tue, 04 Nov 2025 00:55:34 GMT  
		Size: 142.5 MB (142460611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318977d9d7e1d1559e7f7de03c42b5040378712aa9ac6d08a1f1b7f4c498a6f2`  
		Last Modified: Tue, 04 Nov 2025 00:55:47 GMT  
		Size: 69.7 MB (69688148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be06be2370d0b6a6fa791659271834f0acbe3b17b2d27e39ddb7ab5c6239cd6`  
		Last Modified: Tue, 04 Nov 2025 00:55:38 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7a218039be9620ee48e066d70b1308fb5e246407d925b0e871c41f1a295035e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12cbd18c9e98bcbf10ab46ec19f55d8aae50d3d67b4f881295f4a60e6dea8896`

```dockerfile
```

-	Layers:
	-	`sha256:064e9a146d02c99c97eb22ff005be28ea0af309454ccad6dc3a6127e9be6c553`  
		Last Modified: Tue, 04 Nov 2025 10:36:32 GMT  
		Size: 7.4 MB (7421525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:125c94d8bc98e0bfd1289cf3ac4bc3436d862dde83fc71730af95b5154529482`  
		Last Modified: Tue, 04 Nov 2025 10:36:33 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json
