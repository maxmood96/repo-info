## `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:c50efb62538d616daa215c273b43e624c89a24f1dd5cf5c82b2b9bb1f2d26834
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

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

### `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:90acd9136059c32611e964778657c6f1f16cbbb4dde88470d9a1617161de1b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241863747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da9315b124b27d9c7df8aa29e6c7a6acb913272a473bc0d4acdf17b82bd9c82`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6613664525b58457eec67c7df72abf23f57dbd705080696eceb3c83191736df1`  
		Last Modified: Thu, 24 Oct 2024 09:15:02 GMT  
		Size: 143.4 MB (143360984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfc1662c7db0f6681318a8c6e102650d6e41de2417d12f235f347c6e29227b8`  
		Last Modified: Thu, 24 Oct 2024 09:20:32 GMT  
		Size: 69.3 MB (69345381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5ddf2d25b09f9e6daf63544e9429d726a97924cea6dc52f68b4d08f5649df0`  
		Last Modified: Thu, 24 Oct 2024 09:20:29 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7975b899d043be951bb62add2de34f1a8e0a273cd07866cc1359fc420bd8722`  
		Last Modified: Thu, 24 Oct 2024 09:20:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e3b6268ce5d0bb088be207b4bcb18e6f039bbdc21b9c53c71bab336e8a057ad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4942188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4991b776b5cb91e2a621f6a02765366b337a8200d88769a480986c8685e25c`

```dockerfile
```

-	Layers:
	-	`sha256:22d135fb63878741445d2d5086250db054bf6b0e0a1ba450ca9d79a3eb121ea5`  
		Last Modified: Thu, 24 Oct 2024 09:20:29 GMT  
		Size: 4.9 MB (4926358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c89fd4d47685d5bb5f88155dadf8c63896e73c862d28cc8f3ac0a208ac255087`  
		Last Modified: Thu, 24 Oct 2024 09:20:29 GMT  
		Size: 15.8 KB (15830 bytes)  
		MIME: application/vnd.in-toto+json
