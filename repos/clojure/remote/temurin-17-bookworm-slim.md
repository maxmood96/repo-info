## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:f2e59113602cc9813da356e213326aa6cf469058c756f757899abd657d80d9e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3c3bf3e20e25bf9121ac21615c0217876c0bb985246af91828f74f5b71e71e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242061985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250870ec9c03c5332520e2c00d0b0628fb670992d8cbf0c86087a3983c00ad55`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c493070157550d28ab55aa355583ee57bcda99e6eeb4c0347be50863926de88`  
		Last Modified: Tue, 03 Dec 2024 03:19:56 GMT  
		Size: 144.5 MB (144536645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf37d405c146679c918e479fcadc4bd3f440b51ff0535c76f09d2dde4e0428a`  
		Last Modified: Tue, 03 Dec 2024 03:19:55 GMT  
		Size: 69.3 MB (69292721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57e231f12ec9cd6abdbcd7b722cee064f16d6cb6e8d1c6f9678e83f0088d77c`  
		Last Modified: Tue, 03 Dec 2024 03:19:54 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f598324f1b4673c57e87e035ec4d87fc6c28d3d537eeab80163cd8d1ed91b5f2`  
		Last Modified: Tue, 03 Dec 2024 03:19:54 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9d70d41eff01ae39d939b253362c66cbfbcb8f4afd97c298a45fc746ef2cf865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4935259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07642b763f1a90e40f997ddd760962b767278c83be53ceedf87b96a152c2afb`

```dockerfile
```

-	Layers:
	-	`sha256:ca992ef7be3871db9b9ed8d9f0148afba060130eef5bd1a2d66d75bc17583565`  
		Last Modified: Tue, 03 Dec 2024 03:19:54 GMT  
		Size: 4.9 MB (4919380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7c13de99c1233897f569dc05bbe4124ceb388a149814ef94e35a652cd572998`  
		Last Modified: Tue, 03 Dec 2024 03:19:54 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7423646698e32874569a99c3eb570ea925b30235e157f4766679d067b38ec1db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241854078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca775a6069db6b1c00b53cbc09caca36c0bfa8670f15e5c51a54bd41780a214`
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c5d41bfe745c6af4de4be9a0503d5f4ef52f33df043735185d7e7ffc08e3a0`  
		Last Modified: Sat, 16 Nov 2024 05:29:55 GMT  
		Size: 143.4 MB (143360977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ae83d7efb37de65a10794f039dc951bc8a95ba9a9b989bb503a730ea575199`  
		Last Modified: Sat, 16 Nov 2024 05:34:25 GMT  
		Size: 69.3 MB (69334702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4bcb6576baa3446695401e5e4086ea59e4934b861b742f714d5723c5cd538b`  
		Last Modified: Sat, 16 Nov 2024 05:34:23 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d6c71c9a7201c7ce92ae6218b95f6c9113c8823fe38adc7835a26006dd3158`  
		Last Modified: Sat, 16 Nov 2024 05:34:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b7545e5c819ab61d4d39154313e90534399be090d45c2fead363188a78c85a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4942391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa9e63e6a355cd849b288515da7e54a77296283361f9b0522544bde059b2755`

```dockerfile
```

-	Layers:
	-	`sha256:d3a73ab928391eb985f944149bd61376655e4438ea2e21b867bd88ff35aec17b`  
		Last Modified: Sat, 16 Nov 2024 05:34:24 GMT  
		Size: 4.9 MB (4926394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4036a5405e69473104ef43e3cd0ae5376015bf6dd4acaac53588f7e0943d68ed`  
		Last Modified: Sat, 16 Nov 2024 05:34:23 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
