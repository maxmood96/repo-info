## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:b778a7117c1be4119b0c0fdd4d524011a9a0cfb696d2a95e72d66761167dfdc9
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

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

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

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bdc77610da2246224ef5bc642a302e0a71aba2d5e35e9b8f699597e68c7cc220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241174665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f583c23296dfbcdbd65d28fa8dcd86aecfb0e74d0ae201e5bec05d9b5f02445`
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
	-	`sha256:fb5cf058475776582e9e64a646c76b474fe20722c0592878e59918c738320dbf`  
		Last Modified: Tue, 19 Aug 2025 03:50:35 GMT  
		Size: 143.5 MB (143542112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f07b2e01a24e9ce321e14aa2cc745a4b094f44cd1bcda6ade0454b8985b97e0`  
		Last Modified: Tue, 26 Aug 2025 17:42:09 GMT  
		Size: 69.5 MB (69549509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5467f4a4094cfbee234aa6efe4267f6c20e9cf235f42884f1d93366b3d43f2f`  
		Last Modified: Tue, 26 Aug 2025 17:42:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d247203cd97295ecfc33cdb2fca70890563e824572b2582fd24412ec1a1e5887`  
		Last Modified: Tue, 26 Aug 2025 17:42:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1c1fc7e9e5ba0a791197213a6fb262f2306cec7c476e1acb710c126228e33841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c518025ba8375354d7a139f4aecb23e677da33c024c0e267bd76512c3aa3cd6`

```dockerfile
```

-	Layers:
	-	`sha256:da1587e21988dcd8eb85a5d559c4def87e3ddb3a9958c093133f02895f705e40`  
		Last Modified: Tue, 26 Aug 2025 18:37:39 GMT  
		Size: 5.1 MB (5117034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2a8e9ddac51fa831263ea1846643ea3d30b2283c849ab9c10ad8753a290f97c`  
		Last Modified: Tue, 26 Aug 2025 18:37:40 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:8684f72bd27c34396b8bb7e27057d9ab70207fa5b0f022dd85f939c4b5173e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251951368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5682560b647549c4b2fa3641438c9fecdd8eaa2f61083372b115ee7847acb4`
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
	-	`sha256:4f775e155906486b3af9c87541a33fa50508312260cb346dd22a54dd5f4b81a2`  
		Last Modified: Sun, 24 Aug 2025 06:13:53 GMT  
		Size: 144.4 MB (144372832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9934c6c89352d393c8067e20c792bb57995ec4decbb3759b67aac8b6ede12763`  
		Last Modified: Tue, 26 Aug 2025 17:55:34 GMT  
		Size: 75.5 MB (75504071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0a405f98e3eaf7a14cffd9cd50c9dde522175604fa74342d3b825ed8dbf3e1`  
		Last Modified: Tue, 26 Aug 2025 17:55:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31502d7e7e82ebe7c54518978a151a432e76efc324527de7a8fab8031c1b526`  
		Last Modified: Tue, 26 Aug 2025 17:55:28 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0281f6d8114155016e6ff5aa69bb4cce2e853e54bc8c53cd7d456c1ed1ce908e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedc8651844b1bccb3ce6005dbe3289d14ab7545310f70eab66c43e99d71bfb0`

```dockerfile
```

-	Layers:
	-	`sha256:781e1e480ac4658c761a51ca523dd91000b69ad46459d90f2d82d4bc3a478b3d`  
		Last Modified: Tue, 26 Aug 2025 18:37:45 GMT  
		Size: 5.1 MB (5116431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22f890ba8f220f31cbbc785f80861df8cb9d330273cce1dcc20d64b8c990e5ab`  
		Last Modified: Tue, 26 Aug 2025 18:37:46 GMT  
		Size: 15.9 KB (15927 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; s390x

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

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

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
