## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:5ff7f35f2f88ca83db6f21c53d6c35a79add472904034f63bd76ea2c7211e8e1
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

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:4f1d9a9a88b4dab42fdf5f0f1a82abb020eba7bcbfc081d76d162c4e99080679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272507319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc68f1c222f6c7e87cba370def49db23e3693bc356a4a076c5c677fa0cad272`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:43:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:43:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:43:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:43:34 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:43:34 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:43:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:43:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:43:50 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f32787a72998c99c9fafcb13629e678f5ee1effaeb4bfaa78e69fdaf1e6b223`  
		Last Modified: Thu, 04 Jun 2026 17:44:18 GMT  
		Size: 145.9 MB (145886263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5621999ea1ac1e27fd616bd2ff9daf7c50c60f0d00a0e0007fd016d2e0080308`  
		Last Modified: Thu, 04 Jun 2026 17:44:14 GMT  
		Size: 78.1 MB (78124978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b35260a4116387cca0851eea05d55f4d97cababbc72b9667f846883aaa11b61`  
		Last Modified: Thu, 04 Jun 2026 17:44:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4235d1fa532ec34617814f2ad0ca39961828cc2f80c1a570da53c660d45296c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7409995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dedd8d19a32546f0d1e607a895351124967e3532faed10df240be3bd800fdcb`

```dockerfile
```

-	Layers:
	-	`sha256:88495bc601ae505c4a3fbcf17fe3b58ff1da05d71d58bf36da9a3357ae16bbae`  
		Last Modified: Thu, 04 Jun 2026 17:44:10 GMT  
		Size: 7.4 MB (7395632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b684353e33670d80316857fe5b9de78a4eade443d230520df2ed3ed0d5136057`  
		Last Modified: Thu, 04 Jun 2026 17:44:09 GMT  
		Size: 14.4 KB (14363 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:37edea6c8b1270ef20606a8ee797cedb8570fd30264768b4e3dc461941b45169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269088004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b57c2af935c84d680cc73f4f59c676673e34e35b3383cc3829afb89d2493e7d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:43:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:43:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:43:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:43:14 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:43:14 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:43:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:43:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:43:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eace69c6585a3e754c24681ff35f5e28c0546959bf2eb82cf9bf51a74b08962`  
		Last Modified: Thu, 04 Jun 2026 17:43:53 GMT  
		Size: 142.6 MB (142582228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57725ca5d89716e13cc1c2ab18e44b3719916220d9da7e75a844dcf61b0746b`  
		Last Modified: Thu, 04 Jun 2026 17:43:51 GMT  
		Size: 78.1 MB (78125698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2fc766c0db1e50b7909c1bf21a5ca9a955162608808510f2af4ca4bbdd2b15`  
		Last Modified: Thu, 04 Jun 2026 17:43:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9807be52eb8eb662b20942cf4cb9783aaf9e664cdcb90d9eff1b1df5cfe81544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b818a41f49556ede1816a01be465070659b986573da1c198783b68887f3d2d`

```dockerfile
```

-	Layers:
	-	`sha256:22f4bc8d0f00eadcf78dc25c6f4ac2e249c0d77b4c17de7744084ddc22f18fbe`  
		Last Modified: Thu, 04 Jun 2026 17:43:48 GMT  
		Size: 7.4 MB (7402013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1e00722d7d0df8c1a1f2e76b5fe44eb947932aa439904c5c2e1f0ae4706b6a1`  
		Last Modified: Thu, 04 Jun 2026 17:43:48 GMT  
		Size: 14.5 KB (14481 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:3f2230e1937b96659c9e191700002bb37f0164dc483954d99a6f9438eede6aef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269410312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f4af26956b93eedf2aa3de46fe8dc40b92ba903d87eb5a33cdb574d157dfdc`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:47:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:47:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:47:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:47:10 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:47:11 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:47:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:47:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:47:44 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd9dc5a9f698e91b12b1467b7637f73943248991b66286c4adb373e93e4a55a`  
		Last Modified: Thu, 04 Jun 2026 17:48:31 GMT  
		Size: 133.1 MB (133110195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67baff48f2fb740cb9b58c99889751fc6fb36f7716775b3afd54893c0d419994`  
		Last Modified: Thu, 04 Jun 2026 17:48:30 GMT  
		Size: 84.0 MB (83959274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97170153d151b39c93a714ee8ac9104e995669928f855f9e4da4e7d710d8a35d`  
		Last Modified: Thu, 04 Jun 2026 17:48:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:515ccd69540234c6832d73ad86ddb2ce1f0acc50e8901a9a1228d55ca3a2660c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7414642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebbee4fa0b4468c7831e614c8ff450813bf840299f4a3de105430235df311aa8`

```dockerfile
```

-	Layers:
	-	`sha256:0ab7327b989a39c4761bf3351f22731d4f54ff08f820cc8f345f3bd83ef7d5f1`  
		Last Modified: Thu, 04 Jun 2026 17:48:27 GMT  
		Size: 7.4 MB (7400233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:246aa680ba4407b809257fabff7c68ba2735378b29a887cff164b1dfd637fab7`  
		Last Modified: Thu, 04 Jun 2026 17:48:26 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:e97178c1c9b55f62cd3b2b8d95da76362c0bd79f5388d463ad960950da602702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.7 MB (250734494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb817ed2319abc8bd1b815c7e6ca4f30fd12948df2c6b7425dde6dc85921785`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:40:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:40:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:40:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:40:07 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:40:07 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:40:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:40:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:40:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac49fd538b5309e2488498a57ffad63ecfccbf655dbc77a5d9779e16c146505`  
		Last Modified: Thu, 04 Jun 2026 17:40:58 GMT  
		Size: 126.7 MB (126651735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4505fc14c3c6cd31f0663669f225efa0d06f99449db6e075298df5ba20582111`  
		Last Modified: Thu, 04 Jun 2026 17:40:59 GMT  
		Size: 76.9 MB (76926524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312039516f6e21a139d3432da21117d46b0366b2d8176a55c6be68598d910fb5`  
		Last Modified: Thu, 04 Jun 2026 17:40:57 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:14ceaad56d225613155dc6e4e4c2cb589ebb7643345099775d5c9aa7b7fcaa5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370819d4b0eb0802372811a4c4b735a321615a03ac8751a616e1f92093dd1d50`

```dockerfile
```

-	Layers:
	-	`sha256:a062c6cac4ead580365e8212b0750eb69f177aae9e3ee0020ce2376388a55329`  
		Last Modified: Thu, 04 Jun 2026 17:40:57 GMT  
		Size: 7.4 MB (7386955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1119e742c47c02b3e33de036116399cc1351d72dddaa72353a2e9e2ea317dc93`  
		Last Modified: Thu, 04 Jun 2026 17:40:57 GMT  
		Size: 14.4 KB (14363 bytes)  
		MIME: application/vnd.in-toto+json
