## `clojure:temurin-21-tools-deps`

```console
$ docker pull clojure@sha256:b0a9b9661878925a15b4c9373a704398948bdaa477793260fa85ea8cf935570d
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

### `clojure:temurin-21-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:8a05f505a25bedb315d6953153743f8fc780361a5a343d7298445615e3e567e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.9 MB (287870466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cfc699802b29ee659167d8d716abafdabe1f85d3d649365c9524362919b611`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:35:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:32 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:35:32 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:35:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:35:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:35:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:35:46 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:35:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892b95645418014df7ca7e32d5e0abc7d964b653d5a9bb45edda487be90705ba`  
		Last Modified: Thu, 14 May 2026 23:36:10 GMT  
		Size: 158.2 MB (158166943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c3f72de025852480d99d04e22e5750a870854eb07e7b15ae5676fdf3e70e20`  
		Last Modified: Thu, 14 May 2026 23:36:08 GMT  
		Size: 81.2 MB (81213801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f1b4c8ce6f757500496c4e1b2f6225704e9b403f01e88073b431ba8aa8ee21`  
		Last Modified: Thu, 14 May 2026 23:36:05 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97610979f4c5ce057163c301101e28b08bc6a65d18604f9ba41e4ad96b1aa2ef`  
		Last Modified: Thu, 14 May 2026 23:36:05 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:64ed0f134d9c733dadf787789ef3eff3d4dd77b94bdb491e7cccb5571e8e74d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7398079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a881f8516f197c22d6fcdfbe5e7993d38afc40f2e48bbbe8bdb6a48521dc644e`

```dockerfile
```

-	Layers:
	-	`sha256:ba4164d26f67bdf791da55358453b36db82d566f085e0ac32d19a2cd00a407c5`  
		Last Modified: Thu, 14 May 2026 23:36:05 GMT  
		Size: 7.4 MB (7381463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1868278498f0e53e42c51246e60ab4c0741199909dc7369f416ece9900ed309`  
		Last Modified: Thu, 14 May 2026 23:36:05 GMT  
		Size: 16.6 KB (16616 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6cb93076555219c67257fc30d9fbfbe0337236e2916650e6fb5c66a68cc27d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (286032325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c4782c0b596bf8a02eb21c3f68e66b65fa7cd045ce3323d551860c9a7275356`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:35:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:42 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:35:42 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:35:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:35:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:35:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:35:57 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:35:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0e4de089cba8e2206da3e52c8f7ca28828b9d757752180f6f0f44e2e00176d`  
		Last Modified: Thu, 14 May 2026 23:36:23 GMT  
		Size: 156.5 MB (156461324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dad6c183717e258e24349fe6696d3ad924c27699bd8982f39f3d01f8e9e96ab`  
		Last Modified: Thu, 14 May 2026 23:36:21 GMT  
		Size: 81.2 MB (81196807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81a8951c680f4a8ecffb729d8c52a26a132c0ceb04281f76481ca2a524db845`  
		Last Modified: Thu, 14 May 2026 23:36:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c433991f19f955f4eecf68b5b21712cfe78dbcecee014a927e48832bb99452`  
		Last Modified: Thu, 14 May 2026 23:36:18 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:e987f4b4ec0daaba77a1ee4180c8681b73e0c92266b894fa9750c966bdcace90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7404007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852349abf7c4ea69d1d005bc07d9322939dbd96fcf6e51197f1ce9a3727191a8`

```dockerfile
```

-	Layers:
	-	`sha256:355f8adaade84721325db62563444064f70ffdcc83a658bab636b75608805547`  
		Last Modified: Thu, 14 May 2026 23:36:18 GMT  
		Size: 7.4 MB (7387250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abf8cb11d107a8f47278e4079be97d39f66aa92550c70555a16ff6572e6343c4`  
		Last Modified: Thu, 14 May 2026 23:36:17 GMT  
		Size: 16.8 KB (16757 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; ppc64le

```console
$ docker pull clojure@sha256:03eb431969b120d29558d07c3bc65bc0641f1af38160d745cc4fe2b78cd18464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297714379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee79bfef3831faa1d034986ec5956899c5b4c2912027d912fc6b8d974085e64`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:36:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:36:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:36:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:36:33 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Sat, 09 May 2026 02:36:33 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:47:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:47:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:47:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:47:03 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:47:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa7fc9485b4fb59cd58fcb71fcd4db3dba936648eb297bdcd72a79d669b2338`  
		Last Modified: Sat, 09 May 2026 02:37:42 GMT  
		Size: 158.3 MB (158343237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78f104974f6b9ef51df71482653e9a1fd8b52c544f296415e22f23abeb3730e`  
		Last Modified: Thu, 14 May 2026 23:47:41 GMT  
		Size: 87.0 MB (87033311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10ecde6c0aace729019fb511c974a09a1273e5ff6437cb98031167b372c4801`  
		Last Modified: Thu, 14 May 2026 23:47:38 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c18b2590b08df7be54054c127e04821e5f73d3f953ab8bab83f43f03d780870`  
		Last Modified: Thu, 14 May 2026 23:47:38 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:1a7e250613d7378612a6ed827ee78b5ae08294733854627b76b77723f29130e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7402412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd568c58235812ba49ff75e8b93af9a2af30d3fed80d12d331c5967a5493a0fa`

```dockerfile
```

-	Layers:
	-	`sha256:1b36260a0dabba34e3accfe6d342052fc120d6e531321616e0cd984aaf0a14f3`  
		Last Modified: Thu, 14 May 2026 23:47:39 GMT  
		Size: 7.4 MB (7386691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2796a4cb5eb6bf02afe5d01076fe5cbecad163b084f9c06a43cb67bc7d43d65c`  
		Last Modified: Thu, 14 May 2026 23:47:38 GMT  
		Size: 15.7 KB (15721 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; s390x

```console
$ docker pull clojure@sha256:644919b09cc1042335d0b709611331f86430e0d73d194efda91f6800329bc3a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274562300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7281caf99fe065b96a71c9fcac3e6ffbc0dbd8b0ca6d1dc23a4ff16460c7ee1f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:35:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:42 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:35:42 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:35:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:35:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:35:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:35:55 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:35:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25cec1d73807144f8a4fcd73c3f56fbd2782d89baf163adc3be7c86ee3ad419`  
		Last Modified: Thu, 14 May 2026 23:36:27 GMT  
		Size: 147.4 MB (147388349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f949cbed0845fb29f479c25c3e0067548d2088304ec1d4da4302ea220febf501`  
		Last Modified: Thu, 14 May 2026 23:36:26 GMT  
		Size: 80.0 MB (80024884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8736682671971469b49d817d5657d60f74396f720d5b85260b14fcb21ae3c4`  
		Last Modified: Thu, 14 May 2026 23:36:23 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c7d87e5ea17e27490d4b88b1d0800f6395977425d28ddcad5e7377af4ffa16`  
		Last Modified: Thu, 14 May 2026 23:36:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:0a9e4e574d6f7ca9e6b8aee6f90779f406d9fcc263f4cb00d50d21bea6eccc1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7389398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2569a0d8a8880cd0669dbe770eaf92773f59c00011c889e2cc521e41515563ab`

```dockerfile
```

-	Layers:
	-	`sha256:61d6977b151130263797a0d2c7e3ff00b0e79ab9dfd5f60f8b9ef92717f54635`  
		Last Modified: Thu, 14 May 2026 23:36:24 GMT  
		Size: 7.4 MB (7372782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edf8b2d11741a399018d5bb3e9dc18273966fb6b5b27b420c80e95ae866e7559`  
		Last Modified: Thu, 14 May 2026 23:36:23 GMT  
		Size: 16.6 KB (16616 bytes)  
		MIME: application/vnd.in-toto+json
