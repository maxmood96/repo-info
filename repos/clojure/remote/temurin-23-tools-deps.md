## `clojure:temurin-23-tools-deps`

```console
$ docker pull clojure@sha256:f032488f710bcafa007d5a2bcd13400760a14bc48ed159f6975867020bedd3fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps` - linux; amd64

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

### `clojure:temurin-23-tools-deps` - unknown; unknown

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

### `clojure:temurin-23-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0b50047c6c13d48a973deaa542b97482c788b395e86de2c87d72370fe142f1c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.6 MB (293628876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d1443e4667ab45c0fff19e759ced679093a3e875813928dff0a8b45eed71920`
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
	-	`sha256:f72374e05c5fc01256ab2bbc23ee7744b5db54d404aac7042df98fa6ce9ce8f3`  
		Last Modified: Thu, 17 Oct 2024 08:27:41 GMT  
		Size: 163.3 MB (163252799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c02996c20eec70b7b6be0d70ffc26515007dc650ac86b317c732113f4f286d0`  
		Last Modified: Thu, 17 Oct 2024 08:32:36 GMT  
		Size: 80.8 MB (80790058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0573c624f92dd9292787ac2ba42af96d4ccfa47246e5145fa0d49b9bf81507e1`  
		Last Modified: Thu, 17 Oct 2024 08:32:34 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c38732d38f1ffa6cf16dbc734e4d766fb150c311429f25afc12dd4d3ad342b7`  
		Last Modified: Thu, 17 Oct 2024 08:32:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:3bc0e61afa2ee7fccd2aac0b2a03c53b1d8a3dc9fdbcd3c3ca2dbd610f303188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7209703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3cbe4fc8f4a7e3b50e850ce727fb0bf4cdd300d36c5ba3c4ca2b6e70a5a910`

```dockerfile
```

-	Layers:
	-	`sha256:defd3a071e6bf83d1e6709315ca6ff0c442c223944e3bdc831a1f43b614b953d`  
		Last Modified: Sat, 19 Oct 2024 12:22:08 GMT  
		Size: 7.2 MB (7193238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c4192d95ba817ff69d1d2312af27c097199963e291f4fce37e1b1cdad29775b`  
		Last Modified: Sat, 19 Oct 2024 12:22:07 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json
