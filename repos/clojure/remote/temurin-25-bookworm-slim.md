## `clojure:temurin-25-bookworm-slim`

```console
$ docker pull clojure@sha256:095f69058684957c068ae3687de3d3fc671933126f63bcf6439d0fe2add3bd12
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-25-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1bf5ec6bd2792db93011a1cc17693bc79442f57ca99db1b9fe2d03ad9b89d76f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (189952727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd9c24aab15db2adbdc38d85e0fd27cb4fe7e9d52842c4619935f80e5972b094`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 22:40:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:40:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:40:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:40:26 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:40:26 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:40:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:40:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:40:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:40:40 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:40:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51acc32c7bfb538181c3aebb55fdb6ccc76e605c862b3d85fa89c76f602c7e06`  
		Last Modified: Thu, 11 Dec 2025 22:41:16 GMT  
		Size: 92.0 MB (92045295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cf16be9f1cd6c21200903e97a36e2c7105f2f76e0ced290202f1ad65876b95`  
		Last Modified: Thu, 11 Dec 2025 22:41:11 GMT  
		Size: 69.7 MB (69677977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6fcd0f6a1cca4b41d32af0f4fa3dcb1f693ca10ee0f1f8157d5ae5e63fe2fa`  
		Last Modified: Thu, 11 Dec 2025 22:41:04 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608c556121347b8f058d5c4b1da298ef04546dc9c1669249e148dd44b343eb41`  
		Last Modified: Thu, 11 Dec 2025 22:41:04 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c45a79a6b043d743ba75c8544f77bbb252e5fad7154862065bbaa9d437d66e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5081273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:540aff9b48ddbab1794ab0522953971617f77ad3868ce9a4e4a9ed319d567520`

```dockerfile
```

-	Layers:
	-	`sha256:bdf849b631dc16c3d1d2edfb1d5e8c0ed57350e72e698dff241efcbc7e338518`  
		Last Modified: Fri, 12 Dec 2025 01:44:05 GMT  
		Size: 5.1 MB (5064748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:801d548346e9885bf9ee5b668d21923d475f0c8b0682c30794d82c58c7ec753d`  
		Last Modified: Fri, 12 Dec 2025 01:44:06 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:edd91b4aeddf65193ce033f6b60a1bc40e63265759ff47db10ee2fb1f272365e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 MB (188714450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b79dd5314ef633e6fb0f415d58f127d61addcfbfedce44333f0153695811004`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:09:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:09:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:09:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:09:22 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:09:22 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:09:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:09:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:09:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:09:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:09:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09bb079260f4d2b176b04fe8b5f3cde9a368b6541c1f34cf666fe66c2d9f10`  
		Last Modified: Tue, 30 Dec 2025 01:10:15 GMT  
		Size: 91.1 MB (91052515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68774afc34a000b273ee3b97012223bb8a8456b898d0907abbcc2c40f2406753`  
		Last Modified: Tue, 30 Dec 2025 01:10:15 GMT  
		Size: 69.6 MB (69558688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005c0f752c4bc96dd5afef0bf3a1792c8c20c614903b42ed65a97bde900ba3e6`  
		Last Modified: Tue, 30 Dec 2025 01:10:04 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4922df82b0468dbaeb805adf79d38db8e754816eeeecbd0ee228739229bd5b`  
		Last Modified: Tue, 30 Dec 2025 01:10:04 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1b4527ef3fc09971b1bb331e5a2d6f2ed7313a3dac8bbc6cccca0fe256eefc54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaed7960d3997665aedae683e4f7821a725d633d87f088f0b52e75b9a22cbae0`

```dockerfile
```

-	Layers:
	-	`sha256:03f9c5ad86ac7aa9bcf53192c72ff0de069b0fe7ef689ac86fb48f135ec8e336`  
		Last Modified: Tue, 30 Dec 2025 01:37:25 GMT  
		Size: 5.1 MB (5070530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:869383de83db43ac06e81eabf95baeb6f3923c086b2ba7ef59ae2f4a6994256d`  
		Last Modified: Tue, 30 Dec 2025 01:37:26 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:21fc4ccedeb4ce310e878ed54d4e93370b1ba0e4d8fc0b9b6053c1116b6cf7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199190741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24093edbe8c4e98f35ebd14ad685d7116a9157c09531f5d9a58e6c547182cbd3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 16:24:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 16:24:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 16:24:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 16:24:10 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 09 Dec 2025 16:24:11 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 23:05:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 23:05:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 23:05:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 23:05:43 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 23:05:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:85c696326521b18996e4f030a7e27e2c57ad4956710f12ec3011da2c017e09ad`  
		Last Modified: Tue, 09 Dec 2025 09:15:52 GMT  
		Size: 32.1 MB (32068845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d34f3bc4e2e28ed95aba8ec4d91b1f2ea595dcea02126d32ce2f47b884268f0`  
		Last Modified: Tue, 09 Dec 2025 16:25:49 GMT  
		Size: 91.6 MB (91610770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124559ba349c73d2192f3a5269593fe3cbabed4d5c8b8b4570ae22c0788a607e`  
		Last Modified: Thu, 11 Dec 2025 23:06:36 GMT  
		Size: 75.5 MB (75510084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88719ed04b07676fdd490ba81bc669189bd339f35b5862fccf01c1307e37d2b6`  
		Last Modified: Thu, 11 Dec 2025 23:06:28 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415d426b5e137dc995e3662948282829bf0e64fee38ab6333b6a2f060da6526e`  
		Last Modified: Thu, 11 Dec 2025 23:06:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:001a6392c23f83e713751dd6b2c9fefae1ba789986eb25178976a515ad180e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27637350a240f7b44f4e35ea41b264ced3cb84c829c812a4c63b2880ce379744`

```dockerfile
```

-	Layers:
	-	`sha256:46da68e6487af437ec45d4571cd74d93e14f583052c46eed50a0c23cf4cbe1a4`  
		Last Modified: Fri, 12 Dec 2025 01:44:17 GMT  
		Size: 5.1 MB (5071216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:528df463bbf72ecec11118d1c2754442d595712733f1a96e4b948295bee2239e`  
		Last Modified: Fri, 12 Dec 2025 01:44:18 GMT  
		Size: 16.6 KB (16585 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:2209cbe32c1043e657eed11dc64c2b6d717b0f6a0b4f58810ad98c221089ee44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183583917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a975e9c6d32c5d1f0a1748b99ac4372c6e04b7551f45f87735f09e3a32c1216f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 22:37:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:37:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:37:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:37:02 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:37:02 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:37:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:37:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:37:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:37:14 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:37:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefd33dba0f8f2065a47ad89226f2cbf044b0d318ba2188731b8373eb828056e`  
		Last Modified: Thu, 11 Dec 2025 22:37:57 GMT  
		Size: 88.2 MB (88210732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d63c528381093405b1227b128720ab27b05b3000b45d6a9b8050e356005ab80`  
		Last Modified: Thu, 11 Dec 2025 22:37:59 GMT  
		Size: 68.5 MB (68487716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc86683ee400691c3fa6e4e414abebcc200bf57512d4875af5d502a5d341b448`  
		Last Modified: Thu, 11 Dec 2025 22:37:45 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6c3def9062e23643b319ac7e024f3559479f95b71847e5b84380c337e1ab1a`  
		Last Modified: Thu, 11 Dec 2025 22:37:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:55d75e017a98c8db8fbc1aa5aa4b34d24325a4b73f2ff513364d9e7df2134eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5075142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9367b9aa4779ea0c5748de03d7cdbf64680710e71b91ede12fe1cf4d435dc7a1`

```dockerfile
```

-	Layers:
	-	`sha256:2fef0cacf3473105de242461462ffd81e610eb0ea2c1d3f3459a76e79f87a47c`  
		Last Modified: Fri, 12 Dec 2025 01:44:23 GMT  
		Size: 5.1 MB (5058617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:215fb68868148b53225ffde01a262d4150db61a0e7f692f8acf59575cf8806ba`  
		Last Modified: Fri, 12 Dec 2025 01:44:24 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json
