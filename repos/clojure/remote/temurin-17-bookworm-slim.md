## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:9f8d4171d98f8048942b40f6d9a06a1df67718302081c5ded7eded93d55cbc32
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

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ade5521f51be65c3693d5f1bb8b18f9e8d9e42db7ce72cddbd53a449ded69b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242601018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49bba9e35fe380ae89a7afe621f20d410954d52d9a71936c4acb142895af0e9b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16860d1e903b8955ddb8a1b1f79776484ae7b4bf2fee446faf698bb351b4cd5`  
		Last Modified: Tue, 02 Sep 2025 05:30:35 GMT  
		Size: 144.7 MB (144693308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07aa505b25e27a3b536a7d59bcf93bf1f8aa332fe7913237ff8e59e7b37257b9`  
		Last Modified: Tue, 02 Sep 2025 01:57:05 GMT  
		Size: 69.7 MB (69676412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e46e0a01dae386c073409d5242b33201d7e3e23748cdb778aee10c811c8b883`  
		Last Modified: Tue, 02 Sep 2025 01:56:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ed14f091a7c5ec2b8416e9ae68c21bc275bcfc187b7556f29d4dfdd67364ac`  
		Last Modified: Tue, 02 Sep 2025 01:56:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3281f2ed39c585d361a06acd43e6b4d896503f7a31d90979b7a839d2960825d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5127152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08c909feabedd185ad0250dc9a39785f19011f5d3d2b13c3249d878a1bafb906`

```dockerfile
```

-	Layers:
	-	`sha256:8532596360692ba44a9b1fb2a87de8e35d81e40acc6d9d98a33c4af74e60206e`  
		Last Modified: Tue, 02 Sep 2025 03:38:06 GMT  
		Size: 5.1 MB (5111273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75fe875956b8b60beccef60ecdc2109139be73f870e49617dcd744eb20e0c6b3`  
		Last Modified: Tue, 02 Sep 2025 03:38:07 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e78d44a595c9b616c0394ce521e2463e2291ca10c27bfc32e540afde4b09c1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241174693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06de39660921bc690f00343f23d7ffc78dce8917cb787e6218a56cdd8133da4d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde012a37803ae8d4a55810e28cce7a5f9e24800e73f4082e29682e5c99ccaa7`  
		Last Modified: Tue, 02 Sep 2025 08:38:33 GMT  
		Size: 143.5 MB (143542143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172146344bb74d8c6684bb5470e3385f03d590d49a77245cb79077d8d8f9fa3c`  
		Last Modified: Tue, 02 Sep 2025 08:04:50 GMT  
		Size: 69.5 MB (69549505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4cd66e0dec699aefbb8fe5c06dbee56b2b04ffbf0f2692285062bc8961836f`  
		Last Modified: Tue, 02 Sep 2025 08:04:39 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c79c252e271bb15dac389505988d78a9bcd42275b8c095a653073a346aa1c8`  
		Last Modified: Tue, 02 Sep 2025 08:04:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:56070c66b8944b645dd4358d0b2b317307bb5f2142817b0a8176a00a6b34584d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7265a1e0ce9807e429862eda57fc3b8e9c472479fe114dc093673c891722824`

```dockerfile
```

-	Layers:
	-	`sha256:aaf2f66136ec527d86ea388ed4a904bbf021e32e5adf792ba4a8ffb2874bee7a`  
		Last Modified: Tue, 02 Sep 2025 09:37:56 GMT  
		Size: 5.1 MB (5117034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afe92e463cb9febb0c25a5c83a98336487e6d92777cedde35fbaa19594c23672`  
		Last Modified: Tue, 02 Sep 2025 09:37:57 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2f03b46796762574f0a68eda1a22b9114abbbe9a805898d89353907fcb5011ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251951082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892c8e20dc38105ed45c77f17ea952fb809e8ea95767eba31a2cacfd703c488a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1333c6551e970845b661254c356983b766894ab3ab8ba30f415c3587dfb7eeef`  
		Last Modified: Tue, 02 Sep 2025 08:33:09 GMT  
		Size: 144.4 MB (144372649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9386543ef367bff9fd4c2f9d4d8ac4c891f252671e30085d2aae1ed10d0dc1e`  
		Last Modified: Tue, 02 Sep 2025 08:44:22 GMT  
		Size: 75.5 MB (75503967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02219474d00ce3fe9b424e8ae5c430e434afeb63650ffaca4a1623dfc69c1925`  
		Last Modified: Tue, 02 Sep 2025 08:44:13 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77f16a901b8814e2c129e76aa3ace2e6095a1dcaf84048832690fd0ba038b3f`  
		Last Modified: Tue, 02 Sep 2025 08:44:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fa33fc4b763f121622103221bb231fa08bf2b05f736759d4608bbd2d39d272e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1748c28e78b37ec1d922d94e51510da30493e013d048d9bbb8a398bebdea224c`

```dockerfile
```

-	Layers:
	-	`sha256:b19b857927951b74956332e666a6ae7094e7f7800cd827f1a7aa8bf08cafd6da`  
		Last Modified: Tue, 02 Sep 2025 09:38:01 GMT  
		Size: 5.1 MB (5116431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f530e0e8cbb6c492ee132bef94af1e61f6c2c03e29b2e8bfa6495f4db9fa4a2c`  
		Last Modified: Tue, 02 Sep 2025 09:38:02 GMT  
		Size: 15.9 KB (15927 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b4fee0495755c189e19e20aa4e33a888c7e132026023ab76cba6abd28e987841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 MB (230097232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e0a89152b241c55b87084a393025dce1c3291ed7924558f446ad001f024bf01`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573e4798be5520d3327840802bb8b1bf59c483c98e994c8254f217e7b1fbabd5`  
		Last Modified: Tue, 02 Sep 2025 01:57:43 GMT  
		Size: 134.7 MB (134724286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0eb57c11709a6a06db76a9de2517cb46a3f961d18c679fd3f1a8486007245c8`  
		Last Modified: Tue, 02 Sep 2025 02:03:54 GMT  
		Size: 68.5 MB (68484067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0822b72d16fd8da1a38978d5b9fb1709476257b9ad2ccba80ff6d3139ac6c0f2`  
		Last Modified: Tue, 02 Sep 2025 02:03:41 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8db9c9ec509a1f02aa0a8d8faaa010b591863582316111d829a1e8121296ab6`  
		Last Modified: Tue, 02 Sep 2025 02:03:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:588a84a482ad5d34859dcbbf55055d74b0cf28e53225f86f8dfe992868c21ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5118473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9711f43d26d65ccd74042a7592fd1b8e2421d0ff122570551f191ae56a7e0bb3`

```dockerfile
```

-	Layers:
	-	`sha256:629d4477df20522675cd08cd649190eaa61a9b0f34149b3b448835e87bb17dbd`  
		Last Modified: Tue, 02 Sep 2025 03:38:22 GMT  
		Size: 5.1 MB (5102594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6462a0917c06e5a6a0562b2ef8e29dafd2dabbbeeddec6a2fcb13eab4bad1942`  
		Last Modified: Tue, 02 Sep 2025 03:38:23 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json
