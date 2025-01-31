## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:316d408c8b47827290a0e2749a15356653c8812314fd63ebd514d0a84e4c3d22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:342284496a31f8d8f6abf17c408e66d363a765ae6cc7558c5ab4fee9d4112828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268529568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdbfae895870ec64c953afc4828a96ce7640ab077ad21b2eb3227e7b0c9ab29f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ddbb4804d79c311dba99b3e33e2c34a68afa7c1deb824ce5ebfbaaaccaf21`  
		Last Modified: Fri, 31 Jan 2025 02:17:49 GMT  
		Size: 145.6 MB (145598771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccd62511f44ac4bee8d80d26e3ca27ec7ed337546108bf79ffc5ccae80b7fe9`  
		Last Modified: Fri, 31 Jan 2025 02:17:47 GMT  
		Size: 69.2 MB (69190988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8651b842e78fb6e2d9491322026cfe2f9f104bbfdf95191a257d26de6492692`  
		Last Modified: Fri, 31 Jan 2025 02:17:45 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a7fd2a61c833b7409772db901a5565fe7e5e3ad5af9e26141ba998f7a13ec57c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7238948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c76decb224bf3350eb49a76456f8abf5c48ce4b33ed7f5482d12c4eb88c666`

```dockerfile
```

-	Layers:
	-	`sha256:214a9f0663d44420d6824c318ecb7d76e246ad76ba5397b7d76ca8f2c1fb45c4`  
		Last Modified: Fri, 31 Jan 2025 02:17:45 GMT  
		Size: 7.2 MB (7224696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db1fa8d4d2812272a24d4101367437cf69db0e4fe3e72304b46afea6fb7aad92`  
		Last Modified: Fri, 31 Jan 2025 02:17:45 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:683c870463b877a8b2ae1359ae61d8f6b72fa265d660411a5752ac252b23521f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263943616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa89112bfa4b1cb4f48b6dcdf7333fe9e55364b9b45d5f015d086b9f53eded6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e2f6539b1d85900401de8fbe6efdfd6d2c1014aed65431e403268d1f76052c`  
		Last Modified: Fri, 31 Jan 2025 05:02:53 GMT  
		Size: 142.4 MB (142385524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb648c609a152ba7be74c235d573e0c4265de42c0fbcddeffc62bd0b1a233c68`  
		Last Modified: Fri, 31 Jan 2025 05:07:18 GMT  
		Size: 69.3 MB (69311388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f950274c3a01fac1336e80767e5c7ee31321be28583325cff6254e3ecc56da`  
		Last Modified: Fri, 31 Jan 2025 05:07:16 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9a1af2d69b3c57551cb656cb46af59d0ac7fb1123c5f362489caab5e3b9bfd74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7244783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d5976c45930a65786a73f3ad2b3ca70a896da27dd285ad0e16aeb34caefec8`

```dockerfile
```

-	Layers:
	-	`sha256:fb39181f03f359eaf905b9415e6097d4a661030de5b707dd688529bc1aa801a3`  
		Last Modified: Fri, 31 Jan 2025 05:07:17 GMT  
		Size: 7.2 MB (7230413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76f435c281284cc67ab7a7d5ee02325326ba9357b68673f5048e900527e8ad37`  
		Last Modified: Fri, 31 Jan 2025 05:07:16 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
