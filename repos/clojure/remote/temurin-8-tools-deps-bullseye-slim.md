## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:1c19d5d65b088f962a30915e5faca021a917ab2e34dc379c956699b3e9053bc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3401968c07a71bd11dd9ee4b91b07ae5611ed84c56fa6e7d95c1869a839aa3c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143993811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94fc9bcceb925becf4a1e3c56994e58539f42f3a16681447f234c437d584ca78`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc1fd05587ed0c4c0541e56188dc5d2ce0921cc5a956edac9da6205d70cff51`  
		Last Modified: Tue, 12 Aug 2025 21:34:46 GMT  
		Size: 54.7 MB (54731348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7ed25fb03f3675e1142084de49a93b3c123ed1fd17d384d1bc626ff4042f90`  
		Last Modified: Tue, 12 Aug 2025 21:34:46 GMT  
		Size: 59.0 MB (59005700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a35df5e9cb1077c3262b0ef9b83d35802cd0c21e2d93e6438217c7b42613cb0`  
		Last Modified: Tue, 12 Aug 2025 21:34:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5c46b2b510bd5dcc5c758e519a7767cb5dc1fade62676d1f05633ec05d15a443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd7a7c022d85e20f401aaf9898efed59268e0cc676e44eacf9e1fba94538fdd`

```dockerfile
```

-	Layers:
	-	`sha256:dca240f733fc13f020712143fb1a8ffd4340abb9fa245c0708383f91d0ccdfda`  
		Last Modified: Wed, 13 Aug 2025 00:41:43 GMT  
		Size: 5.4 MB (5429648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f430d5e8f4519ff73a5d7994addb92584fe1cd60eb38a43928644f033a614da0`  
		Last Modified: Wed, 13 Aug 2025 00:41:44 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:87ce8fea640d0e698e82c04ae59344465635efa4fc85515923064fb564591250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141724510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40971c962fc7cb4242aecb626a4b597823e30b181422f8d8570342d52dd037b1`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50196a37ffb2ae0f9558d6439442ff4ccfb2eb771b15f1ed7b2bae1d4ddbf68d`  
		Last Modified: Wed, 13 Aug 2025 14:05:30 GMT  
		Size: 53.8 MB (53835638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d211d55f413a092a6ee44f1457608eaec93daaa84f05c73459d82fd880d85a`  
		Last Modified: Sun, 17 Aug 2025 09:39:55 GMT  
		Size: 59.1 MB (59137737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7144f47e622355f39633d01b55092670edacb7084c134e14a8c8ae061b60b45`  
		Last Modified: Wed, 13 Aug 2025 14:49:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9bcd62d87a77b798ec55e7f96b195f33342467f462cb6f43a177be4027375026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5450485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28ea248baaf2afb1d0379c232873fcefefca4826b40be407a50f13c811c99bb`

```dockerfile
```

-	Layers:
	-	`sha256:953b9828d261b32aa4f13627c9b20b482202ba43ccd2e4f7de7a99851b851934`  
		Last Modified: Wed, 13 Aug 2025 15:42:20 GMT  
		Size: 5.4 MB (5436078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1ded98da584e731423b6887b18afccbb8cece2d0ae425679c48c864cafa8563`  
		Last Modified: Wed, 13 Aug 2025 15:42:21 GMT  
		Size: 14.4 KB (14407 bytes)  
		MIME: application/vnd.in-toto+json
