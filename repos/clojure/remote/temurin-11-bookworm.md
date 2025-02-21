## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:0b0bbdb2fc9919d120fa6a5eac552ee42fffb36a07a6c30452654eabddc5bbb1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:be61dffef5792eb6fab2ae238eca8a8fc4c7dc9382ade1918a2b238b2e8648f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275073791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84fca49aa72af7605e66795c03d883d21f9925dfe369dc26da47702821403fb`
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
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7373b7c1de65ee5a52e5dc573c43aed622ff2edcd2a5e3b544cd5c74b81263`  
		Last Modified: Thu, 20 Feb 2025 02:29:38 GMT  
		Size: 145.6 MB (145598915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b21a85f59fcf164f0d3b94e8000618cc499bebcb02b851178481a0dff30910`  
		Last Modified: Thu, 20 Feb 2025 02:29:37 GMT  
		Size: 81.0 MB (80994544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d7a77495ba8f6d38bc36b0851d6e74465c1aeb93eed181aad62168ccd9b7a`  
		Last Modified: Thu, 20 Feb 2025 02:29:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7c78476318d70121311314babe24645004a043905a23a7510e5c3b1b87895281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7205471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82c14e8401af60a2f9d4e9af1f217112b673801db243cd4df7675d60aaba8d3`

```dockerfile
```

-	Layers:
	-	`sha256:1b198f117326376c34645b3fd6f67f982e59515d0b81b828a0452b66c9c576a8`  
		Last Modified: Thu, 20 Feb 2025 02:29:36 GMT  
		Size: 7.2 MB (7191219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c4c7103ac52274a2e2c0d7f10dac9b50ecf7ec23b23744e014ade6609d8890d`  
		Last Modified: Thu, 20 Feb 2025 02:29:35 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3b67d901b917ac33a3e057f0e98b885f54729849e5e7f79e828fdd3641a891c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271537001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5573bbf79b8d1470285be5c9a72df0531974e47db1c521f67304cfc4ba0ea47d`
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
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb2f9b39fd107c3a1429362c7af01d5399568b883e7f731d9c0e63c44448f26`  
		Last Modified: Tue, 04 Feb 2025 23:33:31 GMT  
		Size: 142.4 MB (142385472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52186036e25f7ee63bcbd75ba1b5f07c1242f84cc983f8bbe931565b3a19098f`  
		Last Modified: Thu, 20 Feb 2025 03:45:16 GMT  
		Size: 80.8 MB (80844332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533f39faceac488ca6c76b0e8243bb06fe36f1141e080932135263917deea619`  
		Last Modified: Thu, 20 Feb 2025 03:45:14 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7edf6742195ccc91561ab6452c11be4f709f04cd9ec68c58fa8164fbfd16fc9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7211969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cfbdded3a6903b924d02c386220984f4e5b131235bc5713f6b8d896a2b786d`

```dockerfile
```

-	Layers:
	-	`sha256:20a8775f2d1d26a85e1d50c5c80424850d0337ceb2b39779dbe3840f51742fa2`  
		Last Modified: Thu, 20 Feb 2025 03:45:14 GMT  
		Size: 7.2 MB (7197600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0160e88901926d2127b183b181259e758d6ac153ffa4c468a909848944d8785`  
		Last Modified: Thu, 20 Feb 2025 03:45:14 GMT  
		Size: 14.4 KB (14369 bytes)  
		MIME: application/vnd.in-toto+json
