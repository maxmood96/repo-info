## `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim`

```console
$ docker pull clojure@sha256:b9e0a80100ad311eafe26f57fafbbf63eacda74a69ade073c4d854e8d293508c
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

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:650991b93218292f9d7c243b888b6344ac752a52da4d364b911a03570206e577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247431646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37300332d3bbb2bf19d151d2fead8b763c83b5fbc8b6278d9e815c552a1ecc88`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:30:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 04:30:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 04:30:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:30:34 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 04:30:34 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 04:30:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 04:30:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 04:30:50 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a516a61e3ae97e3dd7caf1643a75e4bca15109f4cec18c1c68cfd7e1574e1ac2`  
		Last Modified: Tue, 04 Nov 2025 04:31:11 GMT  
		Size: 145.7 MB (145658307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d26cdf51de7fe076cda3939c195587c869c6bea1275780d3f9ad2d7577e98e`  
		Last Modified: Tue, 04 Nov 2025 04:31:32 GMT  
		Size: 72.0 MB (71994592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ac8b9e2b5e21c9ede78f26d3efa4215f37868bfadbb1369dc1bf577eb78bfb`  
		Last Modified: Tue, 04 Nov 2025 04:31:25 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e40b2fd69bc3ad7f4f2411f7e4d343f0d737846f78879cd004902bc16d273060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5290550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4850c6173f7fa15666baf08017f6da5a9907011a0a31abe2002f073314ee2a60`

```dockerfile
```

-	Layers:
	-	`sha256:0d1b3f9f374c40c88cbf655bba2972dbbd3f3e69d0cc251cd06efd32c82819b6`  
		Last Modified: Tue, 04 Nov 2025 10:38:20 GMT  
		Size: 5.3 MB (5276308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19b493252c3dbcc06f979c4388d4878352bb6ae7fd20e9d1e8bf9604f04518e2`  
		Last Modified: Tue, 04 Nov 2025 10:38:21 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ff2581b8fcebd5cbb02b9b97552532bd7c84dfbc6cabf2f7d6b3a7b0d29bc306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.4 MB (244411935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf939c704669f978ed60057b3853b1b856d79bae483eaca9abb6ac0aca83035c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:44:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 01:44:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 01:44:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:44:10 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 01:44:10 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 01:44:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 01:44:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 01:44:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046dcb6c776623e499bcb90943629992e4f4ef7aba7b9e2cc0736005b21feb8b`  
		Last Modified: Tue, 04 Nov 2025 01:44:50 GMT  
		Size: 142.5 MB (142460599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c793d668e2e2d38b374356dd6527423260844a0b198351861eed766810538043`  
		Last Modified: Tue, 04 Nov 2025 01:45:04 GMT  
		Size: 71.8 MB (71808393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf58c429ae122f8eca8f75899ca7beb84cb3806d227cdf38f29af068df75d44`  
		Last Modified: Tue, 04 Nov 2025 01:44:55 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b33a61597f529930a1799e88a8a7cf42e9d7931b08e6d6802cd82280e5f34177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de87c0df90bb81a43a77e4846de26b1f341c3cd07548b92565b043fd43ce01e`

```dockerfile
```

-	Layers:
	-	`sha256:529aac0fd020b3fddc87b55909415de6149c0de111296da5f02115ec80e41e83`  
		Last Modified: Tue, 04 Nov 2025 10:38:26 GMT  
		Size: 5.3 MB (5282695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56da3111609d21d1b0cf332fc2bfee6dc686b2beac23facffc461034b2f6556a`  
		Last Modified: Tue, 04 Nov 2025 10:38:26 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e8aa82c10b108c52aa699ed15bbee0c68aab9c78aaa6815303eb8732eb2337ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243847843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f6d1217b5ef30a619cef54138302f7d97e55d39d42cf1d60756afe3982491d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 13:15:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 13:15:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 13:15:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 13:15:05 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 13:15:05 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 13:20:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 13:20:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 13:20:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075756bad78719f88f0199918d09009fc2e6e1986052db04c6df7dc01db38383`  
		Last Modified: Tue, 04 Nov 2025 23:01:26 GMT  
		Size: 132.9 MB (132853177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284c9f33856764fca4eceb84c447c59fe41ba1f5862fa776d9fa4bd8f4a3d1dd`  
		Last Modified: Tue, 04 Nov 2025 13:21:54 GMT  
		Size: 77.4 MB (77395376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e61f1b2ca78cc59f04ccc2b77b160e5e78340fc1fc70af7ba785f3a6d9485d`  
		Last Modified: Tue, 04 Nov 2025 13:21:45 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e6d501427ed4d2b4185b85593475d2965f432fb03a79ab85d12498593c153734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df011f6c42891743a3294c6ad8f2dc63af932c59ab7d8b6d37c95481b08b02be`

```dockerfile
```

-	Layers:
	-	`sha256:3aa4af1fc51817cf2c2117c3c9801f43618009d07f039b467e6ccb713fa50911`  
		Last Modified: Tue, 04 Nov 2025 16:36:08 GMT  
		Size: 5.3 MB (5280064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db541030dc617db1bcd92afda85ffdc76e261222b670e4a41001220a0ed41966`  
		Last Modified: Tue, 04 Nov 2025 16:36:09 GMT  
		Size: 13.5 KB (13490 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:5172f49696caea8d9f0905233b13f880b49ba813e2664432d060bdf3c6c5f5b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228413925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9393145153a66a7fa2769426024fdeb7132cc1123eb579d8a595f540554efa0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 12:56:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 12:56:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 12:56:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 12:56:19 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 12:56:19 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 12:58:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 12:58:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 12:58:37 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b642dac8b5169c88c346b13e8b1a9342f34959618791aa4ee459f45519f5ef4e`  
		Last Modified: Tue, 04 Nov 2025 12:57:26 GMT  
		Size: 125.6 MB (125622161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e56da7eb3c0a289faf85ab74dd28bdf766a0df30386a5b022a43f05aab7000b`  
		Last Modified: Tue, 04 Nov 2025 12:59:26 GMT  
		Size: 73.0 MB (72953726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d067d8321fcba6afbcd6b9050c4510dd2e15d7ad7742814e1ea7baef91b2ad`  
		Last Modified: Tue, 04 Nov 2025 12:59:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:da8193048d8120a071622f7f856b8c6987f86ca3d813c54a2525a9be7c41c7f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5285678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ad690ede1bd3a3c53770aa12c8b85347088b4b732f9c5020e8c9a5f75e1309`

```dockerfile
```

-	Layers:
	-	`sha256:804d70d4685f9b5f2a612e7bc890dd85a75826d043cf2d7747bde68568ceb0e7`  
		Last Modified: Tue, 04 Nov 2025 13:35:24 GMT  
		Size: 5.3 MB (5272236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afb61a2f41eb2682b2576a0c9e08b509792a6630f48db4c5fcde3fb364c6803b`  
		Last Modified: Tue, 04 Nov 2025 13:35:25 GMT  
		Size: 13.4 KB (13442 bytes)  
		MIME: application/vnd.in-toto+json
