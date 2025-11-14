## `clojure:temurin-21-tools-deps-1.12.3.1577-bookworm`

```console
$ docker pull clojure@sha256:199edb8f53812125824c7ec4afada25ade0cd9973a4bab2a95b993ef4e27a750
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

### `clojure:temurin-21-tools-deps-1.12.3.1577-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:284c750db895c46fd3f7c883ca79e241becd7268b0232a176dcbc8acbbd4b4b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287454264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df921e02e3ef0c56358c8aea401ab0cf0b2cd3f7eb8ba8acc8e4a0d18ea0d06`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:54:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:54:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:54:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:54:25 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:54:25 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:54:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:54:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:54:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:54:40 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:54:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a021455fa7ddf4a144a574fdefd0ca9b6fdb5640391eebaecda41c115781113c`  
		Last Modified: Fri, 14 Nov 2025 02:04:27 GMT  
		Size: 157.8 MB (157825964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237d5a5a65af4ab56a6d4d5a8bc01580c49f358d83e9fd0be8fd67441d72f890`  
		Last Modified: Fri, 14 Nov 2025 00:55:17 GMT  
		Size: 81.1 MB (81146199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25cb6829a00e4c34bd114daccf1158cc99da7de4d48e5856107ac70b93114f3`  
		Last Modified: Fri, 14 Nov 2025 00:55:08 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fa0bf78b7eb8c5254a1deb3ee4fd2d61e13dd56016b113da78189b7266c66b`  
		Last Modified: Fri, 14 Nov 2025 00:55:08 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:cdb00f60aa8ce1adff6c6ac352c6a1cdd6a4937c5b9ee540b80ab63009cbce3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e001c57d55a1774bf60a69a8ef139deff784934ca1eeab18968e566bc4440c38`

```dockerfile
```

-	Layers:
	-	`sha256:096165fed6cab3b8a3b51dea393ae00c86c1d63f79a60502f9a0573dd725a23b`  
		Last Modified: Fri, 14 Nov 2025 01:45:57 GMT  
		Size: 7.4 MB (7378678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:256eba9bfe469f7457e128f2415087680c8dc8f0b8bad72883f1adbf289dd6f8`  
		Last Modified: Fri, 14 Nov 2025 01:45:58 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:760cc2951c4da9bcc8804450c9f6357dbd15be7e8ca2b1bf8d9b2212e00a7e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285499323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15bbce69973ddee157f3b6b9598a75e12ee120c7686381d8ea73e6daea64b3f7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:56:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:56:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:56:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:56:54 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:56:54 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:57:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:57:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:57:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:57:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:57:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7467119bfc596bd98d1505f69217e29b03e020c8947806e9671edcf2d47f142`  
		Last Modified: Fri, 14 Nov 2025 05:03:45 GMT  
		Size: 156.1 MB (156107671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e56dd76fa5d47362ab25b77bf3545378b3907aa7b3eff2ed3dd4e8dae8e490`  
		Last Modified: Fri, 14 Nov 2025 00:57:53 GMT  
		Size: 81.0 MB (81031130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a27e5dc0abc4cfb8a17d4dffdb308fc312735f404f05a9085186f141ee79a4`  
		Last Modified: Fri, 14 Nov 2025 00:57:46 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b19b84daabbe5906334ec51f574c1fe4a7d52fe9a8cf94e328486cd4283043`  
		Last Modified: Fri, 14 Nov 2025 00:57:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b9617e2e85e4c8b9082e068522566e06b0960e5857e2eeb97925ac3f28803553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfc3f4046f9bb7cc47ab986bda7703b43310337f757ebf39e6a6fcae09dbd9e`

```dockerfile
```

-	Layers:
	-	`sha256:6a125a8a0a8249ef24ebb30175578357490ca9a9d11c39041d51458ac6a3a680`  
		Last Modified: Fri, 14 Nov 2025 04:38:44 GMT  
		Size: 7.4 MB (7384465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8182d22eb2548f338848d8503f22cc8bb3d01a936f6304cd43511280b330d050`  
		Last Modified: Fri, 14 Nov 2025 04:38:44 GMT  
		Size: 16.6 KB (16604 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:834c5fcbd7dc2567b41f8baca20bef7020a3f41152f7f1b7ce87cec09d0b7ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297257495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1063c8faa41580c8addec7b1c96f9af9f7167e488515b0fba1c19642e5dee8d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 07:17:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 07:17:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 07:17:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 07:17:28 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 07:17:29 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 07:26:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 07:26:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 07:26:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 07:26:39 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 07:26:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd069eaacaacee31b64c953895fa9fc8bb45cd2a8aecf405c793a6f8a3d56b72`  
		Last Modified: Fri, 14 Nov 2025 11:02:37 GMT  
		Size: 157.9 MB (157942937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587691eebf7e9778a149b399eac5e21c495f2d28a3507ff79b3aeb9cad395815`  
		Last Modified: Fri, 14 Nov 2025 07:27:38 GMT  
		Size: 87.0 MB (86986235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d698d36ef00f7f57a6aa104b858d650cb4142adbd0eae82157c85aef21c2fc6`  
		Last Modified: Fri, 14 Nov 2025 07:27:31 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d494fda8e0d849ee9e18d9438b6183f928de1900a2e14c2969fa55bf55f00a6c`  
		Last Modified: Fri, 14 Nov 2025 07:27:32 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fca7f944457b1023ca2fb7d507d325cfb38254d127157f7be262595989f60ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546f79b44305a96cd9538e5a12ca59bcb2f47b105c2230e327f5bc6834c72ff7`

```dockerfile
```

-	Layers:
	-	`sha256:fbaac36e5594ac9076b674e09d44aa114cb0bbf25af5a5d7b0fef1d00bc5b0f3`  
		Last Modified: Fri, 14 Nov 2025 10:37:16 GMT  
		Size: 7.4 MB (7383904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b233c4eb2066edd8c30405d1c8b5f62ef330f694d275ebad1f6b806d6cc7a66`  
		Last Modified: Fri, 14 Nov 2025 10:37:16 GMT  
		Size: 16.5 KB (16522 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:5685ad58deab4e119c1b2e850d4b27ab83bb9748cf186569f99983715496ab98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274165441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca5b447efccbbb9d96c7d38b01d5d79840ddc66c3d5054105ff2f3552c204d5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:59:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:59:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:59:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:59:02 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:59:02 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 01:01:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 01:01:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 01:01:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 01:01:01 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 01:01:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462e287a2a6a2037bb196d8c5445c5c9a076e490ff81bbdc85238b6e72cd8f3d`  
		Last Modified: Fri, 14 Nov 2025 02:05:16 GMT  
		Size: 147.1 MB (147069831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87c4a7b2980acc5e288f2e186c1c08ce1cd0b1546751a3a5fbbfb1827850836`  
		Last Modified: Fri, 14 Nov 2025 01:01:44 GMT  
		Size: 80.0 MB (79956476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b0f06652b19f37669d9480b515bc51d80b0af5e53169739793526785b086a6`  
		Last Modified: Fri, 14 Nov 2025 01:01:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c64993f8968364f16f8f8d6c5c13f624cfd5226d6d87d28eb7cfe34cde6fbff`  
		Last Modified: Fri, 14 Nov 2025 01:01:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:bea0d744d7ddec9e9b5e06d6f712226cd7ee4b7cfbfe45fba157a84f9201c618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7386459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76e30a94ef0c04aee51fe3c0d2bbb2a7662292fc73842d8e4ae759787117ea15`

```dockerfile
```

-	Layers:
	-	`sha256:b9b7cab41f1581b72c6cf3554812f4ab4018d1f0f77f25f2b229951ccb855ef8`  
		Last Modified: Fri, 14 Nov 2025 01:44:32 GMT  
		Size: 7.4 MB (7369997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f008993294d6d87205790ac457621302847a383ef1fc912dcbf6041ba706c675`  
		Last Modified: Fri, 14 Nov 2025 01:44:32 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json
