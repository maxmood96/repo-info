## `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:276421d642042c64461e76539edac0919425ce725d392b4a919d2ae67e9ecee3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:72cb5f159af5d638fbdd981e72af7566bfedafc1784089e221bb956ec958f9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262820800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606cc154007304811d8fdf5e7f435e7e3c87ad0d637352e4ecc298c45ba51e31`
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
	-	`sha256:7fb59a3d9e55d5a8eca495bcb097361d50f4ebdc8dcc8533f146a6b2011a6a49`  
		Last Modified: Tue, 03 Dec 2024 03:26:05 GMT  
		Size: 165.3 MB (165295086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987338f6bbedc5a744be7eca2f94fc220ed1a1c3695457e20ef15f02d1911596`  
		Last Modified: Tue, 03 Dec 2024 03:26:03 GMT  
		Size: 69.3 MB (69293094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795787dde72fa19b001d6da7a74b02081d66da6ebc6b6690020de7df20897a9a`  
		Last Modified: Tue, 03 Dec 2024 03:26:03 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd248d1244758eb79218edaf74e29b6635c3e80739deeb95601a9fe5de6c476`  
		Last Modified: Tue, 03 Dec 2024 03:26:03 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ea95dba04640a97e8c0953983162cc02c9ef0a7533e42a735dc59d4c677c453f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4940271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d015ec026d29cdc462b14e081ca4db69776e2e687c691eaee0114e2bc3ed78`

```dockerfile
```

-	Layers:
	-	`sha256:39d548795b8367eb343724073ce076cffa95bd21a901d4c72660e36199bf4c68`  
		Last Modified: Tue, 03 Dec 2024 03:26:03 GMT  
		Size: 4.9 MB (4924393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ae75e2e8eb6be9533a6616920161baa4f5970abb13a65d0d1c83196f5adb27c`  
		Last Modified: Tue, 03 Dec 2024 03:26:03 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0f15b80c1cb7a14aa080a15f7959af84434b35ec34e7983729acc388201162b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261774881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63a7d529e8d42e2fe86e53fb759352233bdf1363164582ebd87fa9a78c6c778`
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
	-	`sha256:7e8d146b306dcdab2d600e1d2bf7fb965e385834e6c85bc62b45ef12055a0a4a`  
		Last Modified: Sat, 16 Nov 2024 05:47:39 GMT  
		Size: 163.3 MB (163281818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f128602e54bd4c6a6a199bbfc2436c8df0c0bd2778b5e2aed66a930f47c8b0`  
		Last Modified: Sat, 16 Nov 2024 05:52:31 GMT  
		Size: 69.3 MB (69334665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d43d03368f862722e0a35df5cc1bf3cf3212a01eecce76956ec57261c5b6dc2`  
		Last Modified: Sat, 16 Nov 2024 05:52:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5420ad31490430f22828af4177cba2ad26b527276d02aba00988300f716f3aa4`  
		Last Modified: Sat, 16 Nov 2024 05:52:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2f7680dd9341a1cc17c9a79d3315cf49adcfb476ff79cb4db60e46b2f234ae63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4946781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7dd65f2742dbfce54ea8b6714771ec0d1f4a17ac7898f4b864bd7bce174341`

```dockerfile
```

-	Layers:
	-	`sha256:52eadcd1a2d837ac63a1e2cb442311faa840c1f4320c33894ef09a5c1b2e83de`  
		Last Modified: Sat, 16 Nov 2024 05:52:29 GMT  
		Size: 4.9 MB (4930785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ea424eaa91858d3d567e383aa0f537ded5e01eeb799f825f06e34103945b26c`  
		Last Modified: Sat, 16 Nov 2024 05:52:29 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
