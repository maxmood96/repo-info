## `clojure:temurin-17-trixie-slim`

```console
$ docker pull clojure@sha256:fc3e3efb7648b1328905d887baf1cebd5e57ac5c119572e8e9ac548d5f81fba9
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

### `clojure:temurin-17-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d31ef5e09f76ee885bc2081633ba8e854afb82e6c0189b6d28174af8ebe540e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.4 MB (249411317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a970eaaa5158021bb2eeff5dbc7031917352d3d0cbe210d2e8810b1c08a788`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f92cf1f69c319cdb69ccaf8132403c6d5a5205e230029989256c61fd7737b9`  
		Last Modified: Fri, 03 Oct 2025 08:15:29 GMT  
		Size: 144.7 MB (144693589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fa79671e12fde416f8f15c48d89916a374f65692d5e20840a659daafc122f1`  
		Last Modified: Thu, 02 Oct 2025 08:59:30 GMT  
		Size: 74.9 MB (74938921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc517bd513ab00a7e753eae5047e1e918bbc4c16065bbd86b68d72966f845164`  
		Last Modified: Thu, 02 Oct 2025 08:59:23 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c61141f35082dcc19a387c3c7344998c583084b9e4bf8d6586c75c46fed829`  
		Last Modified: Thu, 02 Oct 2025 08:59:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:90bdc490c454e0a503cfffefec0214f58dfd34c5ccb46695f84c156b177e291f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51040312344672a44abfa30cc29ef377ec78a68b959864f89eabd20bc50ca441`

```dockerfile
```

-	Layers:
	-	`sha256:9b247df295b9bc8aaa4d0fcf9232bb0841d4201a188a5c49ed2531ef8bc078cf`  
		Last Modified: Thu, 02 Oct 2025 12:39:54 GMT  
		Size: 5.3 MB (5256167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78fd0d5246a3fb205a018b8d94f9105b4ae6c4d7dfa76d18b8069a74a5e8d4f3`  
		Last Modified: Thu, 02 Oct 2025 12:39:55 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9a9f4a12eca63603fa676b58fd3926b8dc56422860665a5b80f136d891e1060c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.8 MB (248808496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ef6e65df02f775cff0193c543355941ac08dbc749b3fd3ffa0c938f7afcef0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5399ed326fd58b4d7a833d05957ff9132043ad2f1f25def8e57a0f17aad969d`  
		Last Modified: Fri, 03 Oct 2025 08:16:10 GMT  
		Size: 143.5 MB (143542136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0874591fd9d5091a20524b1121734c9b9bc51739c94d651e3aee239e52a947a8`  
		Last Modified: Thu, 02 Oct 2025 02:45:03 GMT  
		Size: 75.1 MB (75124475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df5ce9fb2fc861f60c142984fbf034a77e64198dedf3ad11a9af32015ba62bd`  
		Last Modified: Thu, 02 Oct 2025 02:44:56 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcedd0f50f3ef0b447ac23d3b3c4572b5c41f682887cb91860325b123aa21ea2`  
		Last Modified: Thu, 02 Oct 2025 02:44:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c2de1827cf231a1a77f8fc32be925f94d48172cd4b966dcb5653c767d03ca58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b655f854c84380fb1d37432927e282f2dd8e799c5ab68d624d80acd5a9bf378`

```dockerfile
```

-	Layers:
	-	`sha256:dd15efe5c56423c71d37ed447828afd42770a32906b8c18c9c9ef56777267dda`  
		Last Modified: Thu, 02 Oct 2025 06:41:59 GMT  
		Size: 5.3 MB (5261936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a71333ab07636eebc6c9547ad6ce475ad24ea0185447b15a10a3e1ee42ff1908`  
		Last Modified: Thu, 02 Oct 2025 06:41:59 GMT  
		Size: 16.0 KB (15973 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:569bba8257e0ce73f565eb99be66f33ae7c62b9170f81f28e946cc7727c66f57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258560327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce8803de4451509f5fafeb8663289eef016aa0834db2edf5081b75362627d27`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853fe8e52f9e951bda35c96ebcb6c1913e1f030c8dea1d41eef5c13089db6c4b`  
		Last Modified: Sat, 04 Oct 2025 20:48:09 GMT  
		Size: 144.4 MB (144372677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ebad59cbf64247a1f2681d9c160146609c730d52094c414c87c78205cdd186`  
		Last Modified: Thu, 02 Oct 2025 09:08:01 GMT  
		Size: 80.6 MB (80588155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8c88deade2b96f83c789dbbc0e9d7cbb6bd83b3218484587b0225c25613a00`  
		Last Modified: Thu, 02 Oct 2025 09:07:57 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8432b373ecd54c04426e0df247228f48d650b1bee0668337f5d24deadccc24f`  
		Last Modified: Thu, 02 Oct 2025 09:07:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ff68ff09c6aea7b3111ab271dd3fd15b115d395c847b82b57c33156afaff66d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d219f1a81739826857d4843de8d17f28e6f1968cef185ec99744e1cf5688c86`

```dockerfile
```

-	Layers:
	-	`sha256:9e2536e64800e438cf97d212da80aed9d53f1c2bc7eeb9265902fab9b1ddd19a`  
		Last Modified: Thu, 02 Oct 2025 09:39:11 GMT  
		Size: 5.3 MB (5260538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c354caeb6d6236352fe0d3bb4911e08146d80984433cd6d314499add0ada9b0`  
		Last Modified: Thu, 02 Oct 2025 09:39:12 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:808f60c33ea9ab1061215344a4e0b9bc79b46beea108e0af47a708a0cdccc458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240340658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8551a2946f40b3b4595d4fecb1fba86209eec04705678c84dd73aa63dc07c21d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e324679feb22478e72d40817a5fb70622140af0793e0b219c335894cee9dd6`  
		Last Modified: Sat, 04 Oct 2025 20:47:57 GMT  
		Size: 138.6 MB (138575693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9570da0b9bd6b88663af279d320d188b90ffc991721442fc30f2a5e5bd154e7d`  
		Last Modified: Sat, 04 Oct 2025 14:18:16 GMT  
		Size: 73.5 MB (73488418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b305174f575c0f7b3142a72c5cc1acc4a0468c4982cb000f08c9adba9a57b74c`  
		Last Modified: Sat, 04 Oct 2025 14:18:11 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a8347c36e117e63ddbc28277f2e51ed3225fdb09681707cb99ad487bc795f1`  
		Last Modified: Sat, 04 Oct 2025 14:18:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f41e7a7e332d1c7c683717d9cef1a77f815b6783afbbaa0bdf3190281e871590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c72005e073ec732e5179545fdba43b8cfe8ed3adcf80edcf7a5e856a48e157`

```dockerfile
```

-	Layers:
	-	`sha256:377670ee890833235de2917da24c786f90ebabac50865812bece24549bdea7d6`  
		Last Modified: Sat, 04 Oct 2025 15:36:28 GMT  
		Size: 5.2 MB (5243712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bbe70d6132f5813501eedde3ce2717f611c0e3d1effe9cbe87cb6bf527370fa`  
		Last Modified: Sat, 04 Oct 2025 15:36:29 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:982f88aa6acc082b1be9dc086d2c18ef9c910ca823295a3665b7f5da201d142d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240125194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c76604a448df7ddd685f0824ada6c8b49e7cd87acdf09c5ba76119d13be04c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a273f5c9c3ebb0cfa0ce46495a97571c2fbd1b6027c2ffebbdf7f10520a2e627`  
		Last Modified: Thu, 09 Oct 2025 23:12:50 GMT  
		Size: 134.7 MB (134723655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca5571cf2da1e2cd85e19fd0282c541c2aaa0e817e8da19fdf5ef046dbcd67a`  
		Last Modified: Thu, 09 Oct 2025 23:18:23 GMT  
		Size: 75.6 MB (75563267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91caffb0c2132c82952a916c04629d25476369f18e286487eb6994e236227292`  
		Last Modified: Thu, 09 Oct 2025 23:18:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1469c4c0a2904700448d77e0bc75eac2817f02c0696f823605563fb3540a1d36`  
		Last Modified: Thu, 09 Oct 2025 23:18:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:03372e5050df5efc8849be00b28cdd9fe253425518b9bd94c21dfaeab00f008a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5267945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720c93b044129d35d108cdbc30fe98ae13ae93f19dde685248fc179ce4a18e89`

```dockerfile
```

-	Layers:
	-	`sha256:33007678471fe0f0932637f02b33546f6448fc73daae4ae56a94ef3fdf67f14f`  
		Last Modified: Fri, 10 Oct 2025 00:38:57 GMT  
		Size: 5.3 MB (5252091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4d2adb4e6ded1a99c482b9022addd7d3caecc715284e68d028e26187920bad8`  
		Last Modified: Fri, 10 Oct 2025 00:38:59 GMT  
		Size: 15.9 KB (15854 bytes)  
		MIME: application/vnd.in-toto+json
