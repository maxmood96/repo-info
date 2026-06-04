## `clojure:temurin-17-trixie-slim`

```console
$ docker pull clojure@sha256:38676985803303f8981a30f66210826974b3c64184d16abd9e3c84fc185d4d25
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

### `clojure:temurin-17-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:106c863b2463a0ec757b9f52ff2886143a7d8111cb76fe2ae09c2b7a6d40a571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244638599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbf4c7952fb54a4451636d07aa3c1133dbc92ace78e6e4511c488f92e5b1d85`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:46:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:46:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:46:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:46:12 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:46:12 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:46:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:46:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:46:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:46:28 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:46:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce31a8e33f6cdebf8845a8e07f768ddda2a75bc191742cdc6dc6d6596e67360`  
		Last Modified: Thu, 04 Jun 2026 17:46:50 GMT  
		Size: 145.9 MB (145905480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ffc201aecde7a004c6fe31fc1bb78474fdcf74dd009a3d0906bbac92b59c40`  
		Last Modified: Thu, 04 Jun 2026 17:46:50 GMT  
		Size: 69.0 MB (68952151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb6af83360b88a68026b4e7f6d956eb3ce55801550244b10dd9f6304ab53ad0`  
		Last Modified: Thu, 04 Jun 2026 17:46:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12728fd214eae2d90a914dcaec30ff4108826d0c12c8df1dd1d226e252f6204c`  
		Last Modified: Thu, 04 Jun 2026 17:46:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6a2be603e76c2e676edf0981cf1d48502b6b5ecc89fcbb0f8e917cc133bbe10c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c9251dc1bba4b665cd5dee770c48e3903d91c463a2e554ebd795e5a68846b4`

```dockerfile
```

-	Layers:
	-	`sha256:0fb37dec9356753cf81b69f62e379613127765c1a1e189539ad3bb77fa6168f4`  
		Last Modified: Thu, 04 Jun 2026 17:46:46 GMT  
		Size: 5.3 MB (5257242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd3036dc4d116c0c825c305acea554e1db06409e5a0f543f54485878467012e1`  
		Last Modified: Thu, 04 Jun 2026 17:46:46 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ad9c4fcdcc610b32988c290758a3fec97e1318e4618912ef571d69b3262edb84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243644571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2fb5d4f38f54fe35161cbb3cda4e225a6ce17cdfa4c63c4c5bb58b27bdcff14`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:45:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:45:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:45:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:45:42 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:45:42 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:45:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:45:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:45:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:45:59 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:45:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4309ee1197a4e7ce49afa804ed183c24661563e155f432f5f8eec8ecac8e3c28`  
		Last Modified: Thu, 04 Jun 2026 17:46:21 GMT  
		Size: 144.7 MB (144724335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f51cc4aebbac140e6c301a1c2f3a6c540afa7be20ccd96d8a01e7659f991185`  
		Last Modified: Thu, 04 Jun 2026 17:46:20 GMT  
		Size: 68.8 MB (68777276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc71f7a27bc44701e68dd9295ddd3c24c0b9ab8523712c95814d3f83bdd68ba`  
		Last Modified: Thu, 04 Jun 2026 17:46:16 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374b6c68b4a75ce60169a8af03dba28103f57a1b92a87f43e8ac525aa9ea70ad`  
		Last Modified: Thu, 04 Jun 2026 17:46:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cf16b8072a3723f7d03f4aee2fd68eb7ccc0d074b47a94ae4762bcc7f74c9638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d26e98994fa6bc038a3fbd776a43dd68a25ff0798060b3fc62a83750d60e6c9`

```dockerfile
```

-	Layers:
	-	`sha256:74b0727976c039385ab7cb2c7f39c2818e8f6ea7cce8f22bd86e04c1a62b3cbc`  
		Last Modified: Thu, 04 Jun 2026 17:46:17 GMT  
		Size: 5.3 MB (5263003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b47a18a3124a8a910321ece5d9ff81b461ffc9285bc5a0939ad01f5af9d184c`  
		Last Modified: Thu, 04 Jun 2026 17:46:17 GMT  
		Size: 16.1 KB (16084 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:bdf5bfa3cf79a469537ef88227d372efad162afbeb1c5694eeeb25f7e6b20d53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253736692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ecbc7eeeff02ca7232ec784e50c6f690d8e7d4f1b5bdc1cfde8d5aa3def2a0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:56:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:56:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:56:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:56:03 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:56:04 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:57:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:57:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:57:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:57:01 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:57:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00b56959c90c5f0fe14cf07141a8ccbb5fba2b1e9b43bac05ab20bc6c254eda`  
		Last Modified: Thu, 04 Jun 2026 17:57:46 GMT  
		Size: 145.8 MB (145766113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fce969075dad3f8234f1b38d92b693985c08aa5da5a3d9c2bf1df9338e3b006`  
		Last Modified: Thu, 04 Jun 2026 17:57:45 GMT  
		Size: 74.4 MB (74369083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fec052117ea57934c22cd72ec755fb81c95ad4b7e7a0a188a63f6096b3d5ed`  
		Last Modified: Thu, 04 Jun 2026 17:57:41 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f523d8e1a558a75fbdf09ee5876900417a47255842c5a5585cd78696aa53e04`  
		Last Modified: Thu, 04 Jun 2026 17:57:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eec43f905b9174fdfb3b97bad417ca1372fdfd4a2ab6ec29496331c7ed312123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ded7ea8818a2115c0a602d5cc4a439358007d122035d2bb9ff618065f20146`

```dockerfile
```

-	Layers:
	-	`sha256:15b0a9eab191f93cd912c57f29a3227a134159644788aec896c8b20926304f94`  
		Last Modified: Thu, 04 Jun 2026 17:57:41 GMT  
		Size: 5.3 MB (5261613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb5dc171f1a5579fe1f444d0ba8f75a0e597394e655c8cbcf6d0fd12bc4d114c`  
		Last Modified: Thu, 04 Jun 2026 17:57:41 GMT  
		Size: 16.0 KB (16013 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:654c926d6aea116872b721f946039b1888f73e339dc6fdfadbe600209b1421bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235689496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e945e0fdeda8f3f1d0839d96f90fd33dcca1079d236de977bdd342bcb16673`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:43:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:43:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:43:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:43:19 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:43:19 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:43:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:43:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:43:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:43:38 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:43:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c332a34932edbc997eb667a3295ae9e92879bf5acfc00e3a9a07ef06bf7a44`  
		Last Modified: Thu, 04 Jun 2026 17:44:09 GMT  
		Size: 135.9 MB (135910437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66c0ff84895e2736800e8ef20a42f34747e645c301c1678b6be87efc5bf01f1`  
		Last Modified: Thu, 04 Jun 2026 17:44:07 GMT  
		Size: 69.9 MB (69932090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93821325406efe867fa234db0010717a509d91363e7e3a4f6d7524d2990b9b66`  
		Last Modified: Thu, 04 Jun 2026 17:44:05 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764d114a85fc229dad8e8578c0795417f521f80fc88b9a7c91281f3f69e58d65`  
		Last Modified: Thu, 04 Jun 2026 17:44:05 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9841d38394275b924c1ed553fb0ef05e602f34c898b7595dec47250768bd7453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5269132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a332e4d1981378765a77932ff48f49c656d41255816f97528e9197618a82469`

```dockerfile
```

-	Layers:
	-	`sha256:6a1017fbb3fca16124a132fc6fb9edd420610b2722defd5b1ec521b508fd1c10`  
		Last Modified: Thu, 04 Jun 2026 17:44:05 GMT  
		Size: 5.3 MB (5253166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4b1141c4993022f6a22983420e156b148a41b13ccf1103da619d47ebddbb80d`  
		Last Modified: Thu, 04 Jun 2026 17:44:05 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json
