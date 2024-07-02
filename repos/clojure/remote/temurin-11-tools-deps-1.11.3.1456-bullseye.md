## `clojure:temurin-11-tools-deps-1.11.3.1456-bullseye`

```console
$ docker pull clojure@sha256:921222d5c888b038138f7d53306cca5c935b4b132bbd8e69e44b893c793ffc6e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.11.3.1456-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:b9902fe362a409fcbc7f2fee1a02bd8f92db510b3e971718682bedb0b4040bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269607981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545d37253bd3c6a9e2f93727d9dde414e8708f73efb9819e44e3aa8f8671da2c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad12865678f4a8dff5371ef93742806d2e3b19c13b44777d1e6fa5d0c6cf80e5`  
		Last Modified: Tue, 02 Jul 2024 03:02:51 GMT  
		Size: 145.5 MB (145505213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1182771352a2c9a1ee644eea5f9807fed6397f79082894cd19948fb3541cefd`  
		Last Modified: Tue, 02 Jul 2024 03:02:49 GMT  
		Size: 69.0 MB (69020763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb3cac681eb092802b09845adbefdce3ea0d456631fb185d2106cd582265f47`  
		Last Modified: Tue, 02 Jul 2024 03:02:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.11.3.1456-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b8795c89f0ce691d95fab2dff8d3fed0c61bdd75ebae64d9896357fcc47ed731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7013654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712425829baf6b5a778af8f4298ca58ce488e100a96e7201b4074103ee8767e1`

```dockerfile
```

-	Layers:
	-	`sha256:eaefd570a606ca9217c12770a5bb4e2f8c4de25f8f82c49a3a02ed701ee5ae01`  
		Last Modified: Tue, 02 Jul 2024 03:02:48 GMT  
		Size: 7.0 MB (6999790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96eedf8bfc13185efc8056a51609266a4dfde65d8c132dbb7ca0ce68588d60b3`  
		Last Modified: Tue, 02 Jul 2024 03:02:48 GMT  
		Size: 13.9 KB (13864 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.11.3.1456-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:74603cb938889c5deb88307a6cde48cf9dbea098fb5b9e23e7ad0742f9d634e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.0 MB (264973439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ffdd15cc3ca195ccec3c63fb199ad2f315fd23a48e11be8fbf2b2e7be47b87`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea49f9e62a428fca7628cb048c62c23b0cc38218d89f23a0c414cc08355b9351`  
		Last Modified: Thu, 13 Jun 2024 11:29:59 GMT  
		Size: 142.3 MB (142304041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ea1e73713f155958889468e183ead867a7245abda1fafcbcbf0be264997a0b`  
		Last Modified: Thu, 13 Jun 2024 11:33:38 GMT  
		Size: 68.9 MB (68929167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c233a84e132ac6fdaee9d48ac36d5ad93a75ea7228ee57cf5eff6915f7421b`  
		Last Modified: Thu, 13 Jun 2024 11:33:36 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.11.3.1456-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6ea6316d85ba19ef17e6fb7c66392525b8a70f1a8e7b2ab4f05163d91f507211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7019873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c93a0a7bbf46eb6fae4de8ca035a23a43472d6610a52ba3e2b7f4f261ba781`

```dockerfile
```

-	Layers:
	-	`sha256:cc4c3e6061b6849d30fbd03fb4a3f9189931b1f25ebf831a7097005ccbbfdb9f`  
		Last Modified: Thu, 13 Jun 2024 11:33:36 GMT  
		Size: 7.0 MB (7005473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9e14d2c719e014f18e8e13431091456ec9b9e1953d965f68bdb10e7f1cd43ef`  
		Last Modified: Thu, 13 Jun 2024 11:33:35 GMT  
		Size: 14.4 KB (14400 bytes)  
		MIME: application/vnd.in-toto+json
