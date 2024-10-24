## `clojure:temurin-23-tools-deps-1.12.0.1479`

```console
$ docker pull clojure@sha256:442c4b0affbf80824e8f319deafaaaebd254205b122e4fe72c6a8b4a0deab9d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1479` - linux; amd64

```console
$ docker pull clojure@sha256:a3062c32fb588e164e8447186567e9f9d6f2a882a8361886bb5f34cb158205f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 MB (295779285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c9a78aab566063d707a4b1d132bc05a6edddf44954216ffe25a7ab27a91474`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
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
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb4f5a4cc339643ef766a5b1d19f72fc33ea13bbba812cbbc41464d79f2a428`  
		Last Modified: Thu, 24 Oct 2024 01:56:57 GMT  
		Size: 165.3 MB (165295134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7f3efb47dd9e002ffd874ccc1340f94c69d9a9f1f2ac89e7bf7d5ec6dcb2f1`  
		Last Modified: Thu, 24 Oct 2024 01:56:58 GMT  
		Size: 80.9 MB (80928084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb98c50b132c472e9d91f8f6d926a32dfdebc87d0cf9ee0d019ca7936066090e`  
		Last Modified: Thu, 24 Oct 2024 01:56:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70647d8697b975aa1aa1d8623291ef49e5dff94e829658ad93dcaa8e8cb13213`  
		Last Modified: Thu, 24 Oct 2024 01:56:55 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479` - unknown; unknown

```console
$ docker pull clojure@sha256:25a55f6577985adb03ae88d0a17c3c27eefa56f67b06a3d46dbfe49cf139a4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7204413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d7c874e800634a902211c119202d9a18df750079833f305b545c6f31cf953e`

```dockerfile
```

-	Layers:
	-	`sha256:69063bddfce85d96656a8f2e282ff4a85ea7f4ea91622dc3602f0b702552ddc8`  
		Last Modified: Thu, 24 Oct 2024 01:56:56 GMT  
		Size: 7.2 MB (7188084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4b7cac4e6ec6b1123f9bbaba155d722ee2dd5bdb7605a9646f33b34d4bb7c71`  
		Last Modified: Thu, 24 Oct 2024 01:56:55 GMT  
		Size: 16.3 KB (16329 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1479` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f0490dc0774fa0ca343a70cd1d33cf83b7ad704505219d3210d79c9e85cb02cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293658069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6361a2e49d82caab39d91d2ba4e5b486cc69dcffb9b5ac22966ab12e876970`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ae4b4414c973b15696a4b086371a7a1cf69de00c5e246ce7e063afef75db09`  
		Last Modified: Thu, 24 Oct 2024 09:36:08 GMT  
		Size: 163.3 MB (163281780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2108f867edf5fd315a94fa0d17e634fc826f07f1806fca24dcd8cc323be08c1`  
		Last Modified: Thu, 24 Oct 2024 09:42:22 GMT  
		Size: 80.8 MB (80790272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7ee3ad95ea250aab1b1a9576c6cde686e9ae9020a953fc66136d16f87eb018`  
		Last Modified: Thu, 24 Oct 2024 09:42:20 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdea1357f979fc4b07a7b7f21df03ae77d94447a83e4b2f8e919deb5fc860ca7`  
		Last Modified: Thu, 24 Oct 2024 09:42:20 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479` - unknown; unknown

```console
$ docker pull clojure@sha256:3d7e564e8e19c9a151f0b3a9d257581b3cfc0c99db82f99d25ec3918fb86a723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7209718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9741232fc17e861d6a3bf20b22f02611607042fd972dd40114aefe814f72bd0c`

```dockerfile
```

-	Layers:
	-	`sha256:1cd60f39f9a89971ef2a3e5c4d65e474b96588a663bd70581f86b2d2a2262823`  
		Last Modified: Thu, 24 Oct 2024 09:42:20 GMT  
		Size: 7.2 MB (7193254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bd17f17244017ba623241016a4b39e47d5e868af199a4f5d6bb792a5dc84aa7`  
		Last Modified: Thu, 24 Oct 2024 09:42:20 GMT  
		Size: 16.5 KB (16464 bytes)  
		MIME: application/vnd.in-toto+json
