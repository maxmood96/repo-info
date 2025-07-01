## `clojure:temurin-8-tools-deps-1.12.1.1550-trixie`

```console
$ docker pull clojure@sha256:a30664e97e64e09b7816997ce40cf50d2bd7342d30079e7d7f9028c7d38dbdcf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.1.1550-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:5d8026d4f353c84bde5ac20658660cb197435f4a8274593ed80e0c8d8dd132d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189334919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c2088a7a7f05429b3627392fce003f104544ba241ef12ba65d557f633bdd5d`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
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
	-	`sha256:b72fed6e2775feec9291a4bd4b416f996dfc503eda11eaa00def55711302b4ce`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 49.3 MB (49263877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde2b75516d94dab4d5ec599991ab4757d6743fcba7495856a5e03d8af57e03e`  
		Last Modified: Tue, 01 Jul 2025 02:38:33 GMT  
		Size: 54.7 MB (54716182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c18b5f4bb396fd8ba34dbd0a2f97d662c975184315777c08c9ac66ed1d8c19a`  
		Last Modified: Tue, 01 Jul 2025 02:37:47 GMT  
		Size: 85.4 MB (85354216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e5e05280a5ad2a3072e9bd5f2b5be831338ecbad139b8d28e1986ac46acdd9`  
		Last Modified: Tue, 01 Jul 2025 02:38:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:41a2ba9fb76ec6b454f7dbbd0858671c141aeecd8b1d3b2463f30cc367a08b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7594975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c196dc5c1b4e2f01cdaca558491b7d878343f1b0ec31c26974e09fc78912560`

```dockerfile
```

-	Layers:
	-	`sha256:a19f8041cc98b2918a0d5ae372db5928dcbd063ba778ac6091ef9b15f7e53dfe`  
		Last Modified: Tue, 01 Jul 2025 06:43:17 GMT  
		Size: 7.6 MB (7580763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:529fd55968e9397ae426f68e9e952d7ebeecda8eb93b97728bc881a5e73d2d33`  
		Last Modified: Tue, 01 Jul 2025 06:43:18 GMT  
		Size: 14.2 KB (14212 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.1.1550-trixie` - linux; arm64 variant v8

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
		Last Modified: Fri, 13 Jun 2025 17:46:01 GMT  
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

### `clojure:temurin-8-tools-deps-1.12.1.1550-trixie` - unknown; unknown

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

### `clojure:temurin-8-tools-deps-1.12.1.1550-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:6bc351a5b447198cdff28921127befc480c6fad362fc28fb34ce7f670cee4a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (196035893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a138a1b41433cf40ebfbd2eaa808e616d66e249c5decbc0540e7f0e27c2d2021`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
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
	-	`sha256:5c6a246a80c20351fe842a314b6b3f8561a5ceaea736decf36fe380b29e53224`  
		Last Modified: Tue, 01 Jul 2025 01:18:57 GMT  
		Size: 53.1 MB (53097236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c704c5e7bf6faeb686430ea5965b30fe5f7b7db2f17dfb3e5c0cac06e198c96`  
		Last Modified: Tue, 01 Jul 2025 08:18:28 GMT  
		Size: 52.2 MB (52167961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50627dd79b4cd3cb8b714f9a80c0761502307f5727674d2b7b80c5e0f2b6315`  
		Last Modified: Tue, 01 Jul 2025 08:25:47 GMT  
		Size: 90.8 MB (90770052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83c17176e6dcf72f716def22aec46915d63254ddaca1724b2f0353681184d11`  
		Last Modified: Tue, 01 Jul 2025 08:25:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:06c2062ddc500a5eaec2b8cbd16a2b92da3d0a98c3286248df822f88e22f2fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7600034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fc4db636de5f8b593f517d5728a04becea2f8afeb369da9c1b35b9251b202b`

```dockerfile
```

-	Layers:
	-	`sha256:f0d0d234a27cb0ee0df7ebc22f42027a5dc16af6643272d5cf5fa5819f420859`  
		Last Modified: Tue, 01 Jul 2025 09:42:50 GMT  
		Size: 7.6 MB (7585773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da0e2fd18418cfd97fe2c1f97a0ff272707ff6e31dbd9dcdfa6c09c624ace6f1`  
		Last Modified: Tue, 01 Jul 2025 09:42:50 GMT  
		Size: 14.3 KB (14261 bytes)  
		MIME: application/vnd.in-toto+json
