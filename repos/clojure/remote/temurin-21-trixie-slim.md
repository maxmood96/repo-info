## `clojure:temurin-21-trixie-slim`

```console
$ docker pull clojure@sha256:6d1c0f1bf229b73c673cc75c6ad8b5ae24339d1250de2219bdf127a73e3aed58
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ee972ea4628b144c8c4d9e51721c99e62f9faa61e275d88bb19e0f96b394b2ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259599974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8beccddd4624baf3afef75490b1fffc89c98e2606801a5e75e05a97c1a3d302`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:55:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:55:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:55:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:55:11 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:55:11 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:55:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:55:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:55:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:55:27 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:55:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c814c7c09ac519d70ffb6062bb9678677735795ef96a10ad280abd46b5a6d5f7`  
		Last Modified: Fri, 14 Nov 2025 07:30:02 GMT  
		Size: 157.8 MB (157825994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c12ea13549d4aeb6d02f81cd327022e937a87845f5413b82fb1b16610296ba`  
		Last Modified: Fri, 14 Nov 2025 00:56:12 GMT  
		Size: 72.0 MB (71994831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6187410fc1aca5ab23a3245b294685bd357676c4efca4d322f185445201aef`  
		Last Modified: Fri, 14 Nov 2025 00:56:04 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af0a3ce66595ef6e5806fd0d032ad04fcde033643cca32f89d650885deca817`  
		Last Modified: Fri, 14 Nov 2025 00:56:04 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:85873205eae3e96218d615de737e7906dd2a3815ca85ab4407d51114049fa010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7306f4d398fe3b8a75acaf8488e701bcbd5d91f61c3a2f664c8729319264b225`

```dockerfile
```

-	Layers:
	-	`sha256:1d4d3c4017cee40e44da195f129d17feb0b3423e3f6f31e78acdb196ff9ce021`  
		Last Modified: Fri, 14 Nov 2025 04:41:09 GMT  
		Size: 5.3 MB (5259271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deabb25fbb91cd11c07724302a6aa2b0efde98bcb7a3170a6167be5204dd2722`  
		Last Modified: Fri, 14 Nov 2025 04:41:10 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:45de16a425188bbde1930c801db613b2732b029f4df5ebcb2606940dad30fd66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258059594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:826e6abaa8dc11f8d8d35cc0c9f3d4c6f06b0efdc626f5f07a78185dadcfb7c2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:56:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:56:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:56:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:56:17 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:56:17 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:57:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:57:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:57:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:57:30 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:57:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1d054dab43f3d356da8ad60eb96cbcb1b333af2139189aafd40e280ad6dd91`  
		Last Modified: Sat, 15 Nov 2025 04:02:30 GMT  
		Size: 156.1 MB (156107673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b95aec5c7af984e9f889a8a4d03d8ae727dda0ecda233cc33582343b178299`  
		Last Modified: Fri, 14 Nov 2025 00:58:00 GMT  
		Size: 71.8 MB (71808582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0a1b15265a24bcaea2b144901cc999d253a03e22883379ecc980d207519a3c`  
		Last Modified: Fri, 14 Nov 2025 00:57:53 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6911afe55de38aed8a90802bde57de4c7206923766828e6380249e1a1abcc8`  
		Last Modified: Fri, 14 Nov 2025 00:57:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:330595f3018dddab53fefbddb3bb7729672f2ede5f073d8112a7386fe3591513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aec4bca1b255d4ddac851bdedd09bc63e2d11f701c47dbe8e5eed21675ba63e`

```dockerfile
```

-	Layers:
	-	`sha256:b3645fd5f20cd480097786f90d97d10fb2b47ed6e73fb2591358bcabc54379d4`  
		Last Modified: Fri, 14 Nov 2025 04:41:15 GMT  
		Size: 5.3 MB (5265040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63b5bd5e46ede64f6c4aa9983a6318f574f17047df43178c4ace332cbe284c9d`  
		Last Modified: Fri, 14 Nov 2025 04:41:16 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:9cf22a1e57a31165d6eee4f9debfbb501171d152b2c112ae8902edc0ed3687ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268939452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08aa7089426d72bf2a87fe2a41a38f7850eef7ec5076d70f861ec73d3fb8a537`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 07:24:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 07:24:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 07:24:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 07:24:19 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 07:24:19 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 07:32:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 07:32:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 07:32:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 07:32:49 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 07:32:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d06d2d74488e794ade9cf41666e84e2b03e4c9b061aa03ab78c9135204b2c53`  
		Last Modified: Fri, 14 Nov 2025 07:25:37 GMT  
		Size: 157.9 MB (157942937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb0dbff41aa4edb4139f1f9f0b9f89eeeb8bd5ed282fe09f762194cb220c322`  
		Last Modified: Fri, 14 Nov 2025 07:33:43 GMT  
		Size: 77.4 MB (77396822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d9fc7e9fd9df2337c25052f3dda03271160b2e95b8ee78cd2789ebf2eb6f84`  
		Last Modified: Fri, 14 Nov 2025 07:33:38 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2531d8f69e34fe933ae59e054256fe4e27234bc4656026b1d00bb39e4b9b3ea5`  
		Last Modified: Fri, 14 Nov 2025 07:33:38 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3cdfddc8c8095ebd371e0f507d3b50446bde8950bca612cdf1b32b41335609ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35db34d81beb86d081bcaa5ac4b93efbc149e6a4b4481fa63314844954607c6`

```dockerfile
```

-	Layers:
	-	`sha256:560d5ab2314223f837791fbb8b09790aa9b3d627c6856b3df45125d76d99411e`  
		Last Modified: Fri, 14 Nov 2025 10:38:59 GMT  
		Size: 5.3 MB (5263642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:782404bf197314cc75a21eab26e74006ba2c4ade2bb1a6d29c81a57381155154`  
		Last Modified: Fri, 14 Nov 2025 10:38:59 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:da2375c19639b356194519a79f19a66b8d9af5c280ef39c376652b6537e054db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.0 MB (258963906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164c348f3a021fd605972b2b85e4747b48de37586ae4b32696b279697bdcbf5f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Sat, 15 Nov 2025 21:45:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 15 Nov 2025 21:45:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 15 Nov 2025 21:45:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Nov 2025 21:45:53 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 15 Nov 2025 21:45:54 GMT
WORKDIR /tmp
# Sat, 15 Nov 2025 22:09:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 15 Nov 2025 22:09:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 15 Nov 2025 22:09:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 15 Nov 2025 22:09:35 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 15 Nov 2025 22:09:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5131465c25b63b9013929a6ddbb0fdc268fccc3764e5911f5216cdadb1f24e79`  
		Last Modified: Sat, 15 Nov 2025 21:54:18 GMT  
		Size: 157.2 MB (157194312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73f1710677ab3d8aa1a9ff3a11e63923076b4afb6efb504551282b793de6114`  
		Last Modified: Sat, 15 Nov 2025 22:13:45 GMT  
		Size: 73.5 MB (73492760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a477bd8309e204fa206b62aa88e036257810b90b9cac4570df9f56a1fd721e6e`  
		Last Modified: Sat, 15 Nov 2025 22:13:40 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2020f9292b10a64c7292c7d268e45e5d494401586f49810e24a5c07df258e920`  
		Last Modified: Sat, 15 Nov 2025 22:13:40 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7a2495fb04ac5e932d6f6b1004c62eda500104432624a1688dc14fac069c33f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2aa80b296e18491aec7b40b4b3709fc0e85559ec49e77d8461ec83fe05e8de0`

```dockerfile
```

-	Layers:
	-	`sha256:0b6a3e7bfa7e149ab989a2d4ea5677c4e2df20c870ce0ea122c8b1b79fbe4dd5`  
		Last Modified: Sun, 16 Nov 2025 01:36:19 GMT  
		Size: 5.2 MB (5248765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88c289111ff27de7b634ff9c86fb65cbf08e045da3e273f035d7be9171318603`  
		Last Modified: Sun, 16 Nov 2025 01:36:20 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:2bc30629f98068fadf120dd52c09d14b633f591e7cb7a5796fc2e92d7bfee7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.9 MB (249861892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a414d9ef3c6deff00e69ff1131ed2e8e86f7f72b490192adcc3e39895cb08966`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 01:00:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:00:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 01:00:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:00:31 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 01:00:31 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 01:02:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 01:02:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 01:02:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 01:02:43 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 01:02:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be32e0cd1b5024cab0eecf981b3706b2b67d3726475f3a177973892118fff5b`  
		Last Modified: Sun, 16 Nov 2025 01:43:22 GMT  
		Size: 147.1 MB (147069832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e44e3a0639a7c01b17a9d1c61d41224f85db675708fd0f33775075c35dfed70`  
		Last Modified: Fri, 14 Nov 2025 01:03:18 GMT  
		Size: 73.0 MB (72953625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859e8ad550e2b036d62c3f39ddf35f98a8b22cb02b5d23142e975961a42bc2fe`  
		Last Modified: Fri, 14 Nov 2025 01:03:10 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3924c8fdcbb3ce7431a594d519bd35e9e16fe7082d35ee11d79728525b1bb1b`  
		Last Modified: Fri, 14 Nov 2025 01:03:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5ae039e2c773fe82d9586e1a4b5ec17ceb276341c008867e02e69902328b7944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a47a793f354e28ea74145bbae1916cb3a51d6e4feeea9e1f43fa435c15afdb`

```dockerfile
```

-	Layers:
	-	`sha256:ef86570ad985eb417cd2e24fc19eb569ce45ee47c6994b113f41e0175cc548e1`  
		Last Modified: Fri, 14 Nov 2025 01:46:18 GMT  
		Size: 5.3 MB (5255195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d34237a54001e1398cfe52e2ddfa5a89ee47d2a48e72b9685c0ac8cf1a476a80`  
		Last Modified: Fri, 14 Nov 2025 01:46:18 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
