## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:41f8d906895f13bd77db5f0c56ac04010fbe1701fcf1734200c796b617559b76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:4c9353fe6695c6a423632c66cbf8de2d6da7e17b9455ee5352ae4fa7cecfbc3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281156056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca19e74216bf8f7b51d12ff750dbc942b01ea1ef5f30a455243549d35c803ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:06:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:06:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:06:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:06:17 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:06:17 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:06:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:06:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:06:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:06:32 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:06:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7979ac319d66a2f01fcd73fa0270fc4d7fcad9de153f0ff753897888b00d22fe`  
		Last Modified: Thu, 05 Feb 2026 23:06:57 GMT  
		Size: 157.9 MB (157857047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77cea35ea402d2b35576d5adcd770c7b7c62fb637644423ee6497f69e7aeb965`  
		Last Modified: Thu, 05 Feb 2026 23:06:55 GMT  
		Size: 69.5 MB (69541709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e4b28aacc5067e4605bdd8548bf81290fb582a32181b8e28144c00969657fd`  
		Last Modified: Thu, 05 Feb 2026 23:06:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6021e56c2599e1f1a371371086204e3eae727b82fe831330448821c6371b3b66`  
		Last Modified: Thu, 05 Feb 2026 23:06:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:39265b52d647d4526c0584623b299190fc625511764ec0ef6aca81e4c8663cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d61cd3f25f818037e648b1f258cb5ed53901190d20f87ccd82c58d36083aa3`

```dockerfile
```

-	Layers:
	-	`sha256:aad77454446ac55bf6847b3a7b3705c50a687d3b0475546fe678295bb808f92d`  
		Last Modified: Thu, 05 Feb 2026 23:06:52 GMT  
		Size: 7.4 MB (7399572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410ac42d219184dfbb6cdb81e3fa17aa5307d81764fbcccbd0edffcc1830ca6c`  
		Last Modified: Thu, 05 Feb 2026 23:06:52 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b109bc0258879eacef9938781e39c6fa6032f7b0a534f8ac60ca0143ca37252d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278085820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5088951166bc94e086b92395dc776c2aad949570623d2b5c425dcd621437398`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:07:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:07:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:07:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:07:14 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:07:14 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:07:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:07:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:07:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:07:28 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:07:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771611c975b206dcf61dca1155e35fb11da5d3aa90f60ff1cbcf54379463d24a`  
		Last Modified: Thu, 05 Feb 2026 23:07:55 GMT  
		Size: 156.1 MB (156133061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fc87c75c7c2c4913d92b3771926b0a93dcb3b026cf7afe08714027ea3cc5c3`  
		Last Modified: Thu, 05 Feb 2026 23:07:53 GMT  
		Size: 69.7 MB (69693397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647a7bd06c33df93b2a9f71e2f96b308bfadf85736292dc449ca544e0256442c`  
		Last Modified: Thu, 05 Feb 2026 23:07:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c593d00dbffdf200fb8075cbf8b2a59ddc5d28e555429515c3be4fa3e31a49`  
		Last Modified: Thu, 05 Feb 2026 23:07:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e96b422ef0f9f915e851a05bf9c77d5f5790f3011e024e814605032c8e68f513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7420567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138210cb240096bb3a6f7e9b4ce128fa062af946a456865b876f7b79fdcb834b`

```dockerfile
```

-	Layers:
	-	`sha256:c3e6a6c323489fd6b9d545e0b57eb0229d514c863c18a4b8055548dc164ad78c`  
		Last Modified: Thu, 05 Feb 2026 23:07:49 GMT  
		Size: 7.4 MB (7404671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b7536f1a8bbb99a2064a94f4b3ce775b0c6c9f471754e2c3d17e539692ab6ef`  
		Last Modified: Thu, 05 Feb 2026 23:07:48 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
