## `clojure:temurin-17-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:0dcefc6dcc8041f835e80e19a12bafb379ff594af55accb4313b8acede66ff7d
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

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f5a2c8b0395f6285f80ba87c62f28e18b89542da846c80cd2a0665a79a415e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246622358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33c77d9862a69f224878320f101f3b39503eca09d6cce32198ac558569e54a3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:43:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:43:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:43:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:43:34 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:43:34 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:43:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:43:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:43:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:43:50 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:43:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6341a718b687b018545ac717f902c91bac847c51bfa12065815f91928273a782`  
		Last Modified: Sun, 09 Nov 2025 04:08:38 GMT  
		Size: 144.8 MB (144848044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03aacaf0d5b0aaad9f764513d8a753469385a2817bc6c9975072d9566a521d55`  
		Last Modified: Sat, 08 Nov 2025 20:20:59 GMT  
		Size: 72.0 MB (71995166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edfc2e214574363b23790c8da890dca1084fe9cda90e55d5076221aa81bd5dc`  
		Last Modified: Sat, 08 Nov 2025 19:29:54 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89544baf39e3e1ef8f884855fb567b394f6a6c24c918a47e0769856a577e7a6`  
		Last Modified: Sat, 08 Nov 2025 19:29:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c188f69db4502651738a3eb40d61897c8a84a6f0e878b8d6fa20e1239d383e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be10f4c55c104fcc0269cf1fbd1b6ba320f6da9c02df303b0dbdc849865a16e`

```dockerfile
```

-	Layers:
	-	`sha256:041ab084e452ce3954dd39237f5f43df1e73bfd69af1f8ca57914552c1c5435b`  
		Last Modified: Sat, 08 Nov 2025 22:45:10 GMT  
		Size: 5.3 MB (5256169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6b0f8de332db54507f5c55e4d3ff52c2a7e02465b2ed7f00a74fc73731725a1`  
		Last Modified: Sat, 08 Nov 2025 22:45:10 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3c0005bd183fe4f24c4e6f679ba2565b7f999f982786e81772007d96e7643847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245631898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84abd29c907fee92ee069a03305166441cdc4c89b1f061ade287786028b948a7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:43:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:43:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:43:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:43:03 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:43:03 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:43:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:43:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:43:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:43:20 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:43:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b2c7be3c3ca592ca6407a378dae4ca778b9bbdc6af201b5808c9c2ae4f30ab`  
		Last Modified: Sat, 08 Nov 2025 18:43:43 GMT  
		Size: 143.7 MB (143680021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b51745023d6d5d03a8b9399566c4696075010e87490b261a93fbbd39c2f9a0`  
		Last Modified: Sat, 08 Nov 2025 18:44:09 GMT  
		Size: 71.8 MB (71808534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3586f0735449d268bb5f252492467f7bc64e6b5b6d868b450dc4d78cc8997bd2`  
		Last Modified: Sat, 08 Nov 2025 18:44:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d75bc9093175c76d53d1383575df4017e4b891f966b14dd078f5849512a133`  
		Last Modified: Sat, 08 Nov 2025 18:44:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:058b2c8c9c94742c77c9a357606b9dc21b0d630d7d3e368732bf9ce81d8ad49c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478aed6bdf1798aa52acf47eca7fbebe31a97e18e864061a9e3da8e8d2500fd8`

```dockerfile
```

-	Layers:
	-	`sha256:9b3e8840729f0ec3daa007f0db21b8010c1e7dae1e7c8cbb7b510fc1a71bfb5e`  
		Last Modified: Sat, 08 Nov 2025 22:45:15 GMT  
		Size: 5.3 MB (5261938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05609d6414c39564522c447186c86de4e21e90ecc4a8f993dd33b6fc78950706`  
		Last Modified: Sat, 08 Nov 2025 22:45:16 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b3c6791b30abb2c1a14180a631ff31a7aa80edfa0a8f240cfb384bba693507c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255521579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfca5044f81bf7604c5ff2f34bae6c81fcac056802811766ef7b184bbce4394`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 21:19:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:19:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:19:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:19:55 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 21:19:55 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:29:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 21:29:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 21:29:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:29:13 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:29:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb56603809314457cab77f3e6ee6113b545a14ddbb276ed775bd25c2e218484`  
		Last Modified: Sat, 08 Nov 2025 21:21:13 GMT  
		Size: 144.5 MB (144525174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e28ae93f90e7fd835148abdc27890eacbf9e003bb8c695276be5364ca92fef`  
		Last Modified: Sat, 08 Nov 2025 21:30:02 GMT  
		Size: 77.4 MB (77396716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e85eac4db7342e20b85648794d7eaf780717f4ad69acb15df9093bc19db6bec`  
		Last Modified: Sat, 08 Nov 2025 21:29:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c47a1ded9293d7822c387439521f3234921247eb0e0964b00ae89e9a7c8240`  
		Last Modified: Sat, 08 Nov 2025 21:29:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:22d9bb5875801c8c859b0a934238c6bc143e40fadd97ee9dc5d0d6d056e7deac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d43d63668f75f8924d51ef60298634aad7547cb2cb1f4d7b581c55badc23b35`

```dockerfile
```

-	Layers:
	-	`sha256:7f74734964fa616e92097901efeb15ed2fd30773b329da98c32d3ffa62cab221`  
		Last Modified: Sat, 08 Nov 2025 22:45:20 GMT  
		Size: 5.3 MB (5260540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23f75110b83273b5a08611da20f5dc8f920968af8c11cbbda80378153e135e09`  
		Last Modified: Sat, 08 Nov 2025 22:45:21 GMT  
		Size: 15.9 KB (15859 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:e2af27f839a32314674eb096104151d0e121ac4d6c8d9b24471711eddd60b077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 MB (237733441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5642be4f40ed491fbed656f9238f5e1d831f31d91a3f81449911721f9643d459`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Fri, 07 Nov 2025 06:12:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 07 Nov 2025 06:12:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 07 Nov 2025 06:12:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Nov 2025 06:12:30 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 07 Nov 2025 06:12:30 GMT
WORKDIR /tmp
# Fri, 07 Nov 2025 06:28:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 07 Nov 2025 06:28:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 07 Nov 2025 06:28:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 07 Nov 2025 06:28:49 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 07 Nov 2025 06:28:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cc304f2c3c9744c65f270710f85e4896b7e5ec0b5533cf4e18986ecc22bec5`  
		Last Modified: Fri, 07 Nov 2025 22:59:10 GMT  
		Size: 138.6 MB (138575660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb5a8117620ac06ecbb88dad4643f5a2f13bf0f3ddb8036214dd220484666e8`  
		Last Modified: Fri, 07 Nov 2025 06:32:38 GMT  
		Size: 70.9 MB (70880953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e15d9e34fa12787a2cc26ebfdb08882bc1c53db057491000392733122958897`  
		Last Modified: Fri, 07 Nov 2025 06:32:34 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9f7ce219ef516c07f4d8bb6a7bca918e989ea6bc5736a2cde1b8cb278e9841`  
		Last Modified: Fri, 07 Nov 2025 06:32:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:408456261372cbb6e235f3da81fb2943bf819d08c3fdd8a523749c55c6148806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251dc8f1107a607c80448197daaf74e70bb46cd91e5bc624ab41e8afda07fbf4`

```dockerfile
```

-	Layers:
	-	`sha256:a4833d35639a15b961745ae189b00eca88bf42e7bd66609c83bad9a03b10bcd9`  
		Last Modified: Fri, 07 Nov 2025 10:36:19 GMT  
		Size: 5.2 MB (5243712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45151ae643882904ac9f76f9b47ce5f71ec07920eb58982f14a93d6471ce9474`  
		Last Modified: Fri, 07 Nov 2025 10:36:20 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:148a63ad14b18eacbef3447f671fbb4f103a46de92a32c8b4d8804927269c42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 MB (237651158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f4d76bce7025013f526371b6c67fd7ed0b5ab75aa540f29ba11ad5ed275447`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 19:40:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:40:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:40:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:40:26 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 19:40:27 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:46:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 19:46:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 19:46:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 19:46:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 19:46:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbf71ad3f6894d76931b880dd5f476e305ae8ab269caecdca1b11a7c4ec76be`  
		Last Modified: Sat, 08 Nov 2025 19:41:12 GMT  
		Size: 134.9 MB (134859044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1031ab380056bc21de8e01750408e5772970f2f70e38eb85e25181b6054ab789`  
		Last Modified: Sat, 08 Nov 2025 19:47:18 GMT  
		Size: 73.0 MB (72953681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00776678fda89bf84ff2debf767ee17bd82e1ad465fbbf2df589fa171f60120e`  
		Last Modified: Sat, 08 Nov 2025 19:47:08 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a53d1bd009c7046ff56ce096e2fac268d81e8b02d105720da648f5a90b1c7b1`  
		Last Modified: Sat, 08 Nov 2025 19:47:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:05573406f2fc5ea4b23b1965300f87ad91f5213b75c570146e13eb7ba7095f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5267905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2fd9fa8f6f331bcbb420d11838201c3f7028d7a87a6808d1abd9e6a8739d9a`

```dockerfile
```

-	Layers:
	-	`sha256:1e42b262baa5d16294946e460706abf084c504e25b2254c278ec78265c026386`  
		Last Modified: Sat, 08 Nov 2025 22:45:30 GMT  
		Size: 5.3 MB (5252093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c231563a9ff1062c5b01d7d09ce88e809a858092db01f32e8746f7b866494e6`  
		Last Modified: Sat, 08 Nov 2025 22:45:31 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
