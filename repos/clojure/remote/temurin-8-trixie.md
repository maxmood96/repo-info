## `clojure:temurin-8-trixie`

```console
$ docker pull clojure@sha256:f4584d9d26c7a98d922f280340b4e1c5ca53c7e3d98ece0d4a121358f998e4a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:6e6cfd9e08266160ab8759c3601bd789fd9b1dfd0545aab71cebb781f6b6762f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 MB (189235993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a3425b97be942dada080eddbf230fe9cb3d453a7cecb07f4593ae9d77c2532`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d8e51f6b7dcdaee60f07f9a13a971abe1be9dc977d52d0849087118f80a1c7d6`  
		Last Modified: Tue, 10 Jun 2025 23:25:45 GMT  
		Size: 49.3 MB (49253859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ded4952a75061e537ce5b6b0df59cdb642c50812c190ce00881d9e8b3cc371`  
		Last Modified: Wed, 11 Jun 2025 12:19:54 GMT  
		Size: 54.7 MB (54716149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c4e2b2d3ed457e9f86347ea4d14be6e4071515aa40eb84a99c492ae182c807`  
		Last Modified: Wed, 11 Jun 2025 12:20:10 GMT  
		Size: 85.3 MB (85265343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a94dc2eb92701500e31f31cd160697a10b09cc26a2345dab1867ac61d5ad240`  
		Last Modified: Wed, 11 Jun 2025 01:30:36 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8a01459198f74e68c96ebd4665ca83e5c389b2d2c527526e22f2e42dc232b48c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7594972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b4bb74e9dc4387373ae9607c47ee464a79e9c193a6454165ec8ec3da1a779b`

```dockerfile
```

-	Layers:
	-	`sha256:5c4dec3f97ec2c7e93a8739e97390d5930f429dd3a5eacac8c2be49a483caefd`  
		Last Modified: Wed, 11 Jun 2025 03:42:29 GMT  
		Size: 7.6 MB (7580759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b823c0147583c806c2da104f742051aea65604e403db6bd2a9211223a289fef`  
		Last Modified: Wed, 11 Jun 2025 03:42:30 GMT  
		Size: 14.2 KB (14213 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e7541a7d5314cea03c9bdf32103f4f45126c3f9ecd4b26af031150ec51fdaf71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.6 MB (188649148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ab9e1e9a524eee7eff07dde80e4404df15cb3ae0384835c420f316c958f74e1`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:546a427a0109bbde3a869c6a4ff1ed90ec74768e7fd82dd00441608d83416632`  
		Last Modified: Tue, 10 Jun 2025 22:52:49 GMT  
		Size: 49.6 MB (49621528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e948c49136968a1b57aa01ee8a86e87fbd22e38d9f9f9e7742582a1e17d4598`  
		Last Modified: Wed, 11 Jun 2025 08:07:11 GMT  
		Size: 53.8 MB (53830497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e1126b74fe1f11b7e5b517238aa668f454f3091c5481a17c6e89de3160e7e8`  
		Last Modified: Wed, 11 Jun 2025 08:12:43 GMT  
		Size: 85.2 MB (85196479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e05cacfc7c9720a94d4a4629306da468782721c29d7afc695921b5dd99323a9`  
		Last Modified: Wed, 11 Jun 2025 08:12:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c925185571c2d8d94ad1060c43502db83bedb86f9341821ac875f54cc66e40e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7602818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769fab0b80f61c2d4a55fd4db2aab6686fcb34b9df232797b91cfffc07ca1b62`

```dockerfile
```

-	Layers:
	-	`sha256:cbcb465af40973bd89ebc4ee1de4a95098c2b9dfb42d7b989550d7290faef469`  
		Last Modified: Wed, 11 Jun 2025 09:43:55 GMT  
		Size: 7.6 MB (7588487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aabb83883e6e2dcfeed4fd08981a49884578c468ed323fcc463ad6d5058b2517`  
		Last Modified: Wed, 11 Jun 2025 09:43:55 GMT  
		Size: 14.3 KB (14331 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:fd117b90e5fdbbb8371ece7bd88a47f1efe5da17de2ba823e99ca20585112060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (196031853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b4a9773a69eb516e2308875588bda11298aaaff37a3b194879d1f329e0ddaa`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:70a0e6b9f26ae2a311f0c79d7ff095922eec7e2aa39f94bd8c4e5b385cfa847d`  
		Last Modified: Tue, 10 Jun 2025 22:52:26 GMT  
		Size: 53.1 MB (53090933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abc54a3170c98b75a60c003d79f9e29f38a1679ccff4013b0ba824c76de419e`  
		Last Modified: Wed, 11 Jun 2025 12:06:49 GMT  
		Size: 52.2 MB (52167952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65c9112b981a6485de86773a602e8540122a70e64fd85a7ca54768190929a8d`  
		Last Modified: Wed, 11 Jun 2025 12:06:59 GMT  
		Size: 90.8 MB (90772324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5217365f82468c4d3f4aa06fd0291ddd41907a6ea29b63ec2f3d8bdddf60f6f0`  
		Last Modified: Wed, 11 Jun 2025 09:20:47 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:df6623480b1491f79f29c0254d643245c8b6800e2d9293c31422a5257b0ee00f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7600028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c2304397b03dbc7c04aee5cf3e318737696638af92b5a390b11d96f3d048d8`

```dockerfile
```

-	Layers:
	-	`sha256:6fb605f3df6b52adbf9eba3854b2d6f43a2f07de78e19b5cc61c4db3a7c0956e`  
		Last Modified: Wed, 11 Jun 2025 09:44:01 GMT  
		Size: 7.6 MB (7585769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1193b8e47603b7d93b04bd4d51ff0a9a95cbdc18b66681c3ff6cec26fca8453e`  
		Last Modified: Wed, 11 Jun 2025 09:44:02 GMT  
		Size: 14.3 KB (14259 bytes)  
		MIME: application/vnd.in-toto+json
