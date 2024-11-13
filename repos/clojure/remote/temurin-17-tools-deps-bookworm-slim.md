## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:03824e9315008349819c53d8e7b821635ebee889b047c8922846b681e38e8b34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:15cb2a2adab6d9696adb3249125d9b34dcad5a7f08f4aaea90b0152131eb0753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243150976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f39fa5980ca013be494dc21e1d0f24eb36e8e583727aaef273867387b8c5a92`
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988817053565a5f4ef1a61105fb0d174a019832ed39d3ba16ebd6f1bef7f5959`  
		Last Modified: Tue, 12 Nov 2024 02:24:15 GMT  
		Size: 144.5 MB (144534782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96fc130e3ff7b34d30c4cc15d4d87a8b5d0fb0d31c033c1da2169a9249fc8a6a`  
		Last Modified: Tue, 12 Nov 2024 02:24:13 GMT  
		Size: 69.5 MB (69487157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0536f598e0f6e53fa75302548930c0ec03a76c8c651f77879056592b0d7e5b7e`  
		Last Modified: Tue, 12 Nov 2024 02:24:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358eddfce183d32d1605742543f4810a641931dcbdaf811a5cd2fe1c4f2c4ef7`  
		Last Modified: Tue, 12 Nov 2024 02:24:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7f9b221f3cf8cdcb7d4c8b7fce09b5d79007f10cd39a75e869e55873c3488f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4936507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5bc7cbdefaa939eb5ae0d087552db00a2a5b125384bf5b53110d1678f14b40`

```dockerfile
```

-	Layers:
	-	`sha256:400bc7998e357bce64cca326d3584b84613feb8731292dab2390e8de656447af`  
		Last Modified: Tue, 12 Nov 2024 02:24:12 GMT  
		Size: 4.9 MB (4920628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2044a9a974f3eb06fd2f6c73ab0c0bf298bed8f8b85eb654f684e5e1811bc2f6`  
		Last Modified: Tue, 12 Nov 2024 02:24:11 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cd618c9ca53f33299a14d01917bf50ba15ae3f37b91c29785782f6eeb0141a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241854289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e2c530afb98f1515bf604688c8bd61e4f51634f0d8f8528083d3c1ec53fd96`
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
	-	`sha256:7a5dac92ec05fd0e8b17827d1d6bf2a927431af444723645640cef84289cd8f3`  
		Last Modified: Wed, 13 Nov 2024 01:18:38 GMT  
		Size: 143.4 MB (143360977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf3903da901b722ab84d3d14ae05019eae2292f572835a2d4ee12d20a801b73`  
		Last Modified: Wed, 13 Nov 2024 01:22:34 GMT  
		Size: 69.3 MB (69334914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b09d57c44a748f4a6bb929b8e17d7ae379ec399b4eb3b63f1a59466c80e3a2`  
		Last Modified: Wed, 13 Nov 2024 01:22:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5232fc4ae7a9ab14b5b7030b895eaeef443de53e854103e7aa1fad82f1e393`  
		Last Modified: Wed, 13 Nov 2024 01:22:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0116263cf9067b5455a82ffb8ad09e91d802fa42fd7e8c4f51ea8c8e74f43463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4942391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b888cd60c166b539a5d3b217d85bfa238a5b646bea26116d0c1b74f02d839a`

```dockerfile
```

-	Layers:
	-	`sha256:b9af495632004e9a885bfb3f37729b496d4cf168c72d7f63ebf62ea503665ec9`  
		Last Modified: Wed, 13 Nov 2024 01:22:34 GMT  
		Size: 4.9 MB (4926394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d601031261039d77d91edce7a1aef8c94544ce4f9f63a049f8cb3c44ac98aefa`  
		Last Modified: Wed, 13 Nov 2024 01:22:30 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
