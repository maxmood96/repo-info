## `clojure:temurin-17-trixie`

```console
$ docker pull clojure@sha256:78857c71573a8967e09544164f74a14d1dd374a8f5c7c34d79484087470d7f46
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

### `clojure:temurin-17-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:39019da29259ed1b2133f750dcd9bfcb9cab01161ac5777b5410615907a325a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280812529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16bacf9031f911056b44182a65e3164ed60def426b315a198803a1f634984d6c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:14:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:14:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:14:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:14:45 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:14:45 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:15:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:15:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:15:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:15:02 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:15:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31bd2fc20b65a809189790d62d3d9e66524b7f070e72109ba9e8220c80e0f5d`  
		Last Modified: Fri, 15 May 2026 20:15:26 GMT  
		Size: 145.9 MB (145905454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d4dfe2aa8bd3c1460e0b95b9cdab0f02607b4edf3116c833884cbf3b035c55`  
		Last Modified: Fri, 15 May 2026 20:15:24 GMT  
		Size: 85.6 MB (85603714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd00f4e72b07073e70bdc77082a8b6a6ea2553e27e89a1b1ff15aa88592ac034`  
		Last Modified: Fri, 15 May 2026 20:15:21 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e73a6899353df564b12e4b2a3c2831f324f4d282f282f733de3b7c48913d12`  
		Last Modified: Fri, 15 May 2026 20:15:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e2595f047b1d1698e0773a4ab87480709a351bf0e665403080188172d82ebf7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97531a8644378ee6edae3793d93dfcaef4d0f98f91f59b2be13ab46d7cee35e8`

```dockerfile
```

-	Layers:
	-	`sha256:8166177ebefc56bc4b0dd1890481365f4d979b8406e9b55ca9e11dd75455cc1d`  
		Last Modified: Fri, 15 May 2026 20:15:22 GMT  
		Size: 7.5 MB (7471382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:194d0533342dba3c08d0013e26068d55a9c10ec3bd997fe4d112d69e08ad5703`  
		Last Modified: Fri, 15 May 2026 20:15:22 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fd00b4752f83f6f873256d8d93279a4b2ce25d34a6ab8746d5ab18002c7b5d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279810091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14041853802157124bbb4519a89dcb73476e8a068b5eb6bdb068f41e0b7bab78`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:14:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:14:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:14:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:14:44 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:14:44 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:15:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:15:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:15:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:15:02 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:15:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca4269185ae790973e4295c490c346aaeb8ce0786647b164714be8ce40b1ca6`  
		Last Modified: Fri, 15 May 2026 20:15:27 GMT  
		Size: 144.7 MB (144724358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a1822d14e65a4606687cc56a04200d1ff1a02fee74ac907c0915649d288fff`  
		Last Modified: Fri, 15 May 2026 20:15:26 GMT  
		Size: 85.4 MB (85415242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3a6d2c11f30d19a0e3566ad0aa62b9adab271d4f78d3d3e2640d20b86f96ba`  
		Last Modified: Fri, 15 May 2026 20:15:22 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4e55073ffdf2eba319106835b0205b3d65fec85990eb65a613fe40d177ac42`  
		Last Modified: Fri, 15 May 2026 20:15:22 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:59f34dd44cf55e64c1483c93c56ee931e0dab224b4a83b75de6ed5be7e486fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7494438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6edc89b1f0a90a0c136302e495828d8d6e49c60dacca61856183e1660d8535f2`

```dockerfile
```

-	Layers:
	-	`sha256:6d12ad3e1424c50cb0191e6577dae052a6441a8bf225132c6aaf319e147517d5`  
		Last Modified: Fri, 15 May 2026 20:15:23 GMT  
		Size: 7.5 MB (7478412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edd9fe5e6568a9d86849225148631dba8051760982533c203b07ee0bae042f58`  
		Last Modified: Fri, 15 May 2026 20:15:22 GMT  
		Size: 16.0 KB (16026 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:fd1b166de2644d5ed3c6835d0f642b5e7c78888489f919d32e4ba9b7d01b6be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289897796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7301adb29f4f724794d4a7b2a3aff2b88f8caf6f60f4dd6a957ec11d4dc051a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:31:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:31:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:31:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:31:40 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:31:41 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:25:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:25:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:25:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:25:33 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:25:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06742bfd6f3a4c91a065b055265b2edf944919541ee9c7934bc1931edc1dd4ae`  
		Last Modified: Sat, 09 May 2026 02:32:54 GMT  
		Size: 145.8 MB (145766111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0ccf94ed9c721debdc00b76ccec5da1cba8395fc372135d831e8998d0ba9f3`  
		Last Modified: Fri, 15 May 2026 20:26:14 GMT  
		Size: 91.0 MB (91007478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea1eeeebf3761a9db0fb3908bffa85c297631425d1c2de6825ccf1dddfe5f2e`  
		Last Modified: Fri, 15 May 2026 20:26:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0e1f2d2a5888f158da0e1efa8eeec94a13386aacdf0020ee336424265d6e6e`  
		Last Modified: Fri, 15 May 2026 20:26:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3a01dd3b2f741666130b5566668de94e901977d38dbeee28bcde9a770aa63d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e548152f25be0b2104fff154a45fe49a539e89d83564c0127390c808e07a373`

```dockerfile
```

-	Layers:
	-	`sha256:da460a52e7e2635f180c562d2c32868b101d7d45bf419c7877724c60c8c0db54`  
		Last Modified: Fri, 15 May 2026 20:26:09 GMT  
		Size: 7.5 MB (7475803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d87e49d7f5eefde215a1a2d2da4af678606d72920b11213dcc32376e07b8972`  
		Last Modified: Fri, 15 May 2026 20:26:09 GMT  
		Size: 15.0 KB (15000 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:1f0f578d30cc3293b3ad27d500964173e6b7398ca41d2842c482c3da3f37501a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271850914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cf9676f922d05b86ce03a957fd79ef09947029e203b5709e909af68c9785be4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:34:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:34:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:34:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:34:51 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Thu, 14 May 2026 23:34:51 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:22:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:22:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:22:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:22:35 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:22:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fa8298eaf2592c145eb3df8dd181759e8c3d5b578a6fb605668478ef706f0f`  
		Last Modified: Thu, 14 May 2026 23:35:36 GMT  
		Size: 135.9 MB (135910407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc22eb9fd97b99684b2f80ca7a8f9db6d96152dfef488291220e8c1c9769e92`  
		Last Modified: Fri, 15 May 2026 20:24:03 GMT  
		Size: 86.6 MB (86567154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d51a673b443d859bd0651c6de9d1ccc85ea3e3bfa2584020ed0509f8a80063`  
		Last Modified: Fri, 15 May 2026 20:23:59 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49ed0d8a21942e5d0fe134054d3930bfe090c92fb2b58a7f87f287ecf9955b0`  
		Last Modified: Fri, 15 May 2026 20:23:58 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8792d015c10b15f8b438f59ea155b5cf1e44b179d76f4ed09cad8ac70ce22aa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:792e1f738026c33f12e75b36105da6f0a3193bfd3a2d6b5ff5cbcd3d18add722`

```dockerfile
```

-	Layers:
	-	`sha256:e1928b343c4dec7c397be86d241bd48c1186bb0196f9dc92ee529702decde362`  
		Last Modified: Fri, 15 May 2026 20:23:59 GMT  
		Size: 7.5 MB (7467304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1792bc953327e18236e7aabf4bbc4f73964f8f6d336b4ae99b5c948f90d08fb4`  
		Last Modified: Fri, 15 May 2026 20:23:58 GMT  
		Size: 15.0 KB (14952 bytes)  
		MIME: application/vnd.in-toto+json
