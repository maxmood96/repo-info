## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:c9f5401cdc2785bdeaa811747443a4fe626414f1d574267dd4e5bd2816cc9c19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8fdf96b18f4bf601deb6e415df7c413e88c53d73d3a028ceafd689291a0c243e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152464501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b3e1170e57a1261c6cf7ac0a75177f679a45db0cb2f1c2b17cab82d5f39a29`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac515e5352f245a7e3af614b365dc70c90aebdf977f0f1ea674d9162bb418351`  
		Last Modified: Thu, 20 Feb 2025 02:29:37 GMT  
		Size: 54.7 MB (54721245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b862997a2c951d4292d44c653b0b32e4a418faed028ec72d935709c8f07c31be`  
		Last Modified: Thu, 20 Feb 2025 02:29:50 GMT  
		Size: 69.5 MB (69530308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e8066a529740d7981f90ab8d84b40cc74523049f7692a11b3a3b4608b36866`  
		Last Modified: Thu, 20 Feb 2025 02:29:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:39bb55c717cc14788ab2d29799150e347b92e6a8bb66f44238da784f91f2b3ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5048467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15d640dc313ca2276f31083b0db1e599042bd868e64aea280ac16ec592713ac`

```dockerfile
```

-	Layers:
	-	`sha256:1bd237957b457c3a4535d71d40e40e212c045473d9a2a0bd218e5a1dfed57b4a`  
		Last Modified: Thu, 20 Feb 2025 02:29:48 GMT  
		Size: 5.0 MB (5034177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98e566b6bcd2ec556d4b424fedc90b8a3656e958da351470e7882ce979c3e78f`  
		Last Modified: Thu, 20 Feb 2025 02:29:48 GMT  
		Size: 14.3 KB (14290 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3b58935c93a98052bccf5616a65e4f9a82b22568e995a2eaabcc85fb9f9e9af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151243606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:021e8e748261d0287502a7169e025ebcc69b6ee6988d75287222ec7c38063b4c`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369cc069c8bd5d579d827d5defd418fea2cc6c0b401c91c66c1194709652d556`  
		Last Modified: Tue, 04 Feb 2025 23:25:04 GMT  
		Size: 53.8 MB (53822735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f897e51b789247d39e01cc3589a08e5be90074749ff78929deec319e18e4140b`  
		Last Modified: Thu, 20 Feb 2025 03:39:50 GMT  
		Size: 69.4 MB (69379347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f081864cb9196c62f26d5d499bb36890fd8a2d826bdde0c29a31cc1ba19339c`  
		Last Modified: Thu, 20 Feb 2025 03:39:47 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1fb94f946084d9f07fdffaf0c9023fac2975ae38cc543a2bf4732aa7f3d109b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9da3ffd5eda9424b6599d9fd659223a5d9d03789e12716b6f83b36d4285820f`

```dockerfile
```

-	Layers:
	-	`sha256:ebf1e72914bf2554353dbf5256ea70ab9a31cb8de7cbecb1694189e6fba0dd77`  
		Last Modified: Thu, 20 Feb 2025 03:39:48 GMT  
		Size: 5.0 MB (5040636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c92cdfc36961f27d477f69304aa46530fb2c5414da3ee473219b67d23a769b8f`  
		Last Modified: Thu, 20 Feb 2025 03:39:47 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
