## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:cbe002a0bff63a9d59c17e89715d14088b75e54738b48846a620bd5ac0cf03ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:30cc9042cf30bf0f338f5a11eb20f9d5788b04b9d00260fcdf7a710db0ad1647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (275049801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054e9646d267b2333d0dca11defe2e0f0a1e5a2b05f2d5474b68131cd2399282`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61a889d840f7bfb98e4ea4c7cf62a1896212502c6fe93f75580d40c3ed6b4b6`  
		Last Modified: Tue, 12 Nov 2024 02:24:14 GMT  
		Size: 144.5 MB (144534744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f30d37bd605978f8d583b610d5b80a9b9738d5de6e77b28530d9d20110ab6e5`  
		Last Modified: Tue, 12 Nov 2024 02:24:12 GMT  
		Size: 80.9 MB (80938325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4dcdefbd4708efa19aeffa0083e8941e69ab0fc2898db57535271974a1e67ea`  
		Last Modified: Tue, 12 Nov 2024 02:24:10 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4e4f8322cd0829a881c336faa3290a66c541a7100bef94ca6ba44bcef11e0a`  
		Last Modified: Tue, 12 Nov 2024 02:24:10 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:49ecc6d8c85b61582fe866239df6f81f694b08ed6ec43a4a09e8dac9506b7efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7198243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a4aacbf92a9134b67a7903d25a77556a28d717be500a73812b3667193db244`

```dockerfile
```

-	Layers:
	-	`sha256:f638bc63f3e9958789142d4c14d432650b42c0ff7308e799024d7fe7be3bcb2d`  
		Last Modified: Tue, 12 Nov 2024 02:24:10 GMT  
		Size: 7.2 MB (7182423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d57c28ddbeeedd3728c7b737dbb5521c48011cff587968257dc7c64ecb4c066c`  
		Last Modified: Tue, 12 Nov 2024 02:24:10 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:179116dc994ce3f4e53d75881b28be0f672379c573e41e2c537da0396244da1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.7 MB (273737235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca1862f4eb94ee6eafaf05a4a8661afbe9946e3a43e54f4c85a75773037d560`
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
	-	`sha256:d6be9297fdd1b50f05a57283e6dbe8e4455d2728758fd4fc2d4c702510853b21`  
		Last Modified: Thu, 24 Oct 2024 09:14:04 GMT  
		Size: 143.4 MB (143360984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efb70d7a7e67334cb84b12216d4f00e5696b9aac03323bdf7c880a388713d6a`  
		Last Modified: Thu, 24 Oct 2024 09:19:44 GMT  
		Size: 80.8 MB (80790236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e8f96afa40605a1611566f93c08a4d399d4183aa106ee907336099c871d437`  
		Last Modified: Thu, 24 Oct 2024 09:19:42 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cacdd3a836a48026b6be8904c6908681f7a1f2f6f051db4aa23380a20daa0f0`  
		Last Modified: Thu, 24 Oct 2024 09:19:42 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:37e1c0f3555c2c7c257db8882bd4250043491f6ee90be14c2bdf2b8447306095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7203913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8ac1c1995e2321d4bb64e2bafc967b9d5f34f1cb195d900735d3cbc72c2d78`

```dockerfile
```

-	Layers:
	-	`sha256:28df1518aac66858fc0f1908b9c92d3f8f644f7455098c8788c91ff2c1fe84d6`  
		Last Modified: Thu, 24 Oct 2024 09:19:42 GMT  
		Size: 7.2 MB (7188155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:988bb27f34148dcad858a86eb3ff097d3ac04ad9ca2937132bc3a8605afea474`  
		Last Modified: Thu, 24 Oct 2024 09:19:42 GMT  
		Size: 15.8 KB (15758 bytes)  
		MIME: application/vnd.in-toto+json
