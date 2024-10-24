## `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm`

```console
$ docker pull clojure@sha256:e98b8e8b260d1c01ed87cffb7360c5950c3398f3fc1620a933dc5ca8c1df98a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:debe9827f7332c4cc1db74896315413f8f4d493ba5ced480da66f25fa9316b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.1 MB (276085103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a653cc59b38cd3ee2115e953ab1e1d9c44c8c50d43e92e369c0abe4034ec93d`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963d254ff9d6cb33bbf47d33e1a9e706b61299172dc378193ca8c0ff74e90d4c`  
		Last Modified: Thu, 24 Oct 2024 01:59:40 GMT  
		Size: 145.6 MB (145601284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3e431e93f9adec6c8ecb369e3de12df94d052cc257e70c8f28abf43447a56f`  
		Last Modified: Thu, 24 Oct 2024 01:59:39 GMT  
		Size: 80.9 MB (80928152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4623f606a171f3138c5bcb30d9833a81802ceb6601e45a18543b018a743239`  
		Last Modified: Thu, 24 Oct 2024 01:59:38 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ceb39cffd07d9af0e380647a6ee3f6390f78c46488b085a018ad1be352519b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7216629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0b0d53327dc64d75c28abc542c5b57d560b8350bc57be1156b4865cd28785d`

```dockerfile
```

-	Layers:
	-	`sha256:0b3f6faf09f4fe153b43a47d5f4180adacb0c05b45a09c00d869dbcdd9ad600a`  
		Last Modified: Thu, 24 Oct 2024 01:59:38 GMT  
		Size: 7.2 MB (7202558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f63710c9c178c320a8ddc1ebb66862bf6a669c58a5179a6cd3c91965fe27e9d2`  
		Last Modified: Thu, 24 Oct 2024 01:59:38 GMT  
		Size: 14.1 KB (14071 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4ae9f16179bbae4731cec637704e85d5d570d0922e3d49d4efabb6dfdc35cd5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272764790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7851cbd8f92975f43e428805248ecbe2ece41a1d78a421914ba138d5909cbb4b`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887acec9ae8608e8242cc2712ca5110681b42182eb911e5fe3d78e161502ec12`  
		Last Modified: Thu, 24 Oct 2024 09:03:11 GMT  
		Size: 142.4 MB (142389122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b689cb2ac0ed8ed9b1f5d7f5864607d71364c9fb26c5b3de608e3fb121e888`  
		Last Modified: Thu, 24 Oct 2024 09:08:53 GMT  
		Size: 80.8 MB (80790046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39dc85ef66eb47bfb8742d6c437d0b55e8f826a3fd46399ab21911c9e7d5a04d`  
		Last Modified: Thu, 24 Oct 2024 09:08:51 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2e317eff326493318c6d7f8d0a39df7fc11646475c6c50f7d14967ee4df5616b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7223128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6032694e3977a80b5b06e8138983e6d2163e8d07bb8af82cbd6fd2a2133f42`

```dockerfile
```

-	Layers:
	-	`sha256:8ccde8d875121c007dfa36773f9750cb689403739cca3c2b2539a7b20135404e`  
		Last Modified: Thu, 24 Oct 2024 09:08:51 GMT  
		Size: 7.2 MB (7208945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a32ab0a2240e586198ec77c3ee75bbfaf35e397eb61c4df87019694139b83a3`  
		Last Modified: Thu, 24 Oct 2024 09:08:51 GMT  
		Size: 14.2 KB (14183 bytes)  
		MIME: application/vnd.in-toto+json
