## `clojure:temurin-21-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:5b2865fa5d60a23690e3f8c35cf2e6c1c77e643364004ce3155f1226d1cff7d1
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

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; amd64

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
		Last Modified: Fri, 14 Nov 2025 00:55:50 GMT  
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

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; arm64 variant v8

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
		Last Modified: Fri, 14 Nov 2025 00:56:57 GMT  
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

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:02efda2ac9640e8024d7b5fd29a41f1431876e47fde74bc25074997de86bb652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268939485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96a6a3497aee07618ae62e07421377cdd3f006926542dbeac770a5725f52f15`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 21:36:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:36:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:36:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:36:25 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 21:36:26 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:45:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 21:45:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 21:45:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:45:31 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:45:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415390733088512f768bce0a8253b48875f9511f6c4dcb6f7f3efc679d791f76`  
		Last Modified: Sat, 08 Nov 2025 23:04:04 GMT  
		Size: 157.9 MB (157942893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1545f45bfd8c83cfe8576d5cb0e50b02bba36aa7758a336d4123fd7de04c4f5`  
		Last Modified: Sat, 08 Nov 2025 21:46:21 GMT  
		Size: 77.4 MB (77396905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed48f8ac6b304228f6c25fbdb29551b60a3c37c793a4374bfa908cc1da56884f`  
		Last Modified: Sat, 08 Nov 2025 21:46:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6f83935703a7b2baab45d71969789604b4e9f4f39624f4f1d796343033c709`  
		Last Modified: Sat, 08 Nov 2025 21:46:14 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3b71f9dcf4538cad2ac747833df63d293997276a9e90f9638514f1977ddd1f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274a50b3b56201f695ec3f22ace9e247de8acbcc1c614c209e61a0599e5b86b5`

```dockerfile
```

-	Layers:
	-	`sha256:713a53f426323fef3e2bfa4dc4fdeb200c445532bfdffb3975c5bbbbb5d6af02`  
		Last Modified: Sat, 08 Nov 2025 22:50:14 GMT  
		Size: 5.3 MB (5263642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de9d9dafede41eb5f71d98643d8e51e4bdc86f5434453f5747d2388a350047e6`  
		Last Modified: Sat, 08 Nov 2025 22:50:15 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:a3ee98d17f4a8fa452c48bd48618a526e7d56da1d3091f86534e5584db3b5627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256351912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c42cdad0071e3192f5c4875888212915a56ce7f236ddd5c0f5104cceb173a7a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Mon, 10 Nov 2025 03:59:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 03:59:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 10 Nov 2025 03:59:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 03:59:39 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 10 Nov 2025 03:59:39 GMT
WORKDIR /tmp
# Mon, 10 Nov 2025 04:23:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 10 Nov 2025 04:23:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 10 Nov 2025 04:23:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 10 Nov 2025 04:23:06 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 10 Nov 2025 04:23:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b159c76c0a400634d8cc831efabe9ffd5180107c11ce3676547a08e780b9fb8f`  
		Last Modified: Mon, 10 Nov 2025 23:11:06 GMT  
		Size: 157.2 MB (157194306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040ac85f6b10e6a562a9e7f19a16556363d9a39a5f51784b160265dc9d131422`  
		Last Modified: Mon, 10 Nov 2025 04:27:13 GMT  
		Size: 70.9 MB (70880780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f615584b65a71701999bf105cbf76e8de3c8a68d11233e22610e9b40622cea`  
		Last Modified: Mon, 10 Nov 2025 04:27:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b684be6f747bca5027a08963ceff50d164213efa29a323704d43e850a752cfdf`  
		Last Modified: Mon, 10 Nov 2025 04:27:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:59dae4c019ca08ac3d983064a8bfc3eaf4042cab20831ac5dba95fe895554855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a039489159abf66ad704ab2cea0ee91990d9d53238504fd40625d7f255c1e04d`

```dockerfile
```

-	Layers:
	-	`sha256:249d4f0c0f4a3e0dc184251acf5d5c496450e369adbf98e8ad790d450bd74a76`  
		Last Modified: Mon, 10 Nov 2025 07:36:51 GMT  
		Size: 5.2 MB (5248735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:352f26dbf0301bbbd5308e3939fd960de325310ef6d8b2b8a88f7f50cab59ac0`  
		Last Modified: Mon, 10 Nov 2025 07:36:51 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; s390x

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
		Last Modified: Fri, 14 Nov 2025 01:01:15 GMT  
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

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

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
