## `clojure:temurin-21-trixie-slim`

```console
$ docker pull clojure@sha256:9c1da968c9cce77a0c83c6860f21256ddce75e97f973d55392561944e1347088
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
$ docker pull clojure@sha256:6d46d4ab0f74b5c62c377149542ff4ec2b5f7bc22b2ced7b1a81aefa4a1e25ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259600040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdce264a0f6c9b9ee2e0246a37cb1ce11a8810f39806a16419b0b9c10756af25`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:45:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:45:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:45:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:45:05 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:45:05 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:45:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:45:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:45:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:45:23 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:45:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab8dabef038ea4c2254df1959e483d283f81810c1ac7b646c4f8469f5de00e7`  
		Last Modified: Sun, 09 Nov 2025 04:46:38 GMT  
		Size: 157.8 MB (157825975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbf18e37887b8f7cee24277786dc5b2d1afbae2cc14103652e4d32991bee227`  
		Last Modified: Sat, 08 Nov 2025 18:46:19 GMT  
		Size: 72.0 MB (71994916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26b89cf0113ec585c115d998445e5f4061389af6ab45d097c1dbd7ed4338398`  
		Last Modified: Sat, 08 Nov 2025 18:46:14 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2680bc1b485b3876b3a2291b0201dc9533f4f0d7248847f9d428ee36166545`  
		Last Modified: Sat, 08 Nov 2025 18:46:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:20022006dfc989a22f91b8a63902fe8c9ee905f0cd206b34a6601e246ba472bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852cd7b662816c9a4193b129d74c09a345434febf785e8224c170e323b2b0392`

```dockerfile
```

-	Layers:
	-	`sha256:ada90a209b12d7bdbdc2afb1c647618757f5c965961cdb1254ee1c4784ec6fb4`  
		Last Modified: Sat, 08 Nov 2025 22:50:05 GMT  
		Size: 5.3 MB (5259271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3961a49834347db71d2418f78c8a830cf12f509feb2fd115660761af8dc3b41`  
		Last Modified: Sat, 08 Nov 2025 22:50:06 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:456d0b344b1fb7d327d8ef546141f36034c7460bf8b65443b4d2c26cda711be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258059564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120f01eb54b15b63841db470d2b2da6cfa8b2cb9b0f2099862e45e48763b4d13`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:44:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:44:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:44:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:44:35 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:44:35 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:44:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:44:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:44:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:44:53 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:44:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32361349a651788a5a7a73151f24b336a90c6ab0292863e83d10d66c3eb5117f`  
		Last Modified: Sun, 09 Nov 2025 08:45:08 GMT  
		Size: 156.1 MB (156107661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6e0457be31c3c4e167b93e2272dd55f1bf1bacb7f728586d624c7c87bd8e1f`  
		Last Modified: Sat, 08 Nov 2025 18:45:27 GMT  
		Size: 71.8 MB (71808561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3513446ae0024a9d5ac6a693aa8cf74d00d59472cb9862cd68cc2597852fb200`  
		Last Modified: Sat, 08 Nov 2025 18:45:21 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4647bd0421ea8940399b5eb3e0c7f7a439b914bd2bb078dae354a6f4389b51b9`  
		Last Modified: Sat, 08 Nov 2025 18:45:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c4aab31401b11824f9e796b295ca1baefdce46a7e64ecf07b26bebec1018556e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaed9a57f8722830912d51a37c3f00a5339eb5957fe58e3e290eb2f1db01b530`

```dockerfile
```

-	Layers:
	-	`sha256:389ab57a59a93123bc4409b5b8cb850998c580a50bac3ff03fab4d4f20c74306`  
		Last Modified: Sat, 08 Nov 2025 19:36:43 GMT  
		Size: 5.3 MB (5265040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:471b521b24e139d7157a8caadc12cfef507bddfb7c55299cddfc3b0b66cf6a41`  
		Last Modified: Sat, 08 Nov 2025 19:36:44 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; ppc64le

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

### `clojure:temurin-21-trixie-slim` - unknown; unknown

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

### `clojure:temurin-21-trixie-slim` - linux; riscv64

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
		Last Modified: Mon, 10 Nov 2025 04:05:42 GMT  
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

### `clojure:temurin-21-trixie-slim` - unknown; unknown

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

### `clojure:temurin-21-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:9de812905729043f07273b7b373760431172fda2fa5e40dfbbec1d7b50ed0a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.9 MB (249861689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7f4c614b6bff8cb0311a54dcb84dbca028c57cb42960c660ebc1869fbf21b4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 20:31:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 20:31:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 20:31:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 20:31:19 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 20:31:20 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 20:36:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 20:36:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 20:36:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 20:36:25 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 20:36:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b891b02a41c144ad667375203af22ef67797f89fef67b5503aca8b9fb1eeb108`  
		Last Modified: Sat, 08 Nov 2025 20:31:59 GMT  
		Size: 147.1 MB (147069879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcdb8f85f8f85d35b3635140f7c8f429cb5789aa916349647b0eebbc5706378`  
		Last Modified: Sat, 08 Nov 2025 20:37:03 GMT  
		Size: 73.0 MB (72953375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273ade99fe70544bf8fa42999d1d0d8c9067ed1e7ba9b5bbdaac581d136a0123`  
		Last Modified: Sat, 08 Nov 2025 20:36:57 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84db03c324127bf4993658b223b2ae36a3a65819102f7aa230aaf6d312172498`  
		Last Modified: Sat, 08 Nov 2025 20:36:57 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:79ba4b5dc09ac220bb493478cff9fa5e2d11ab50cf59ad48e325f0ecf4a456f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592c7bb51cf21eb3ccc599e6e96bba53c60032ea220b4f9ee6b3679e9b9bb020`

```dockerfile
```

-	Layers:
	-	`sha256:b0232943f14674557f27e833a9874a66cbb08e4949e92a38c7b7220fddfdca79`  
		Last Modified: Sat, 08 Nov 2025 22:50:23 GMT  
		Size: 5.3 MB (5255195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ed934cde5c4904a363c861b06a613fb1be14ba8b8058722bc69c50adb6698ef`  
		Last Modified: Sat, 08 Nov 2025 22:50:24 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
