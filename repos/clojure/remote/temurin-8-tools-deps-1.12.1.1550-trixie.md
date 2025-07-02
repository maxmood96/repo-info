## `clojure:temurin-8-tools-deps-1.12.1.1550-trixie`

```console
$ docker pull clojure@sha256:96702888ef5e5aae53a7ba7897918e23157bc2b60ab0748ece00115e5619bd09
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
$ docker pull clojure@sha256:947c2abb291ca9b2799c4551609373e0d30bf75ea4492075fde42b3eac589f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189335823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d255c4aaa299785d48cc0f11cc164237ff409fc7362b22683a47ae16e2bd6fd`
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
	-	`sha256:2121166af06e1412056dcacf68b2efdf4d55cc03422e495b470fab63edd53f5e`  
		Last Modified: Wed, 02 Jul 2025 04:16:12 GMT  
		Size: 54.7 MB (54716181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffeb5103650a881f19dec1a69133ffd3d73b8e94fd92700851bbc6ccfedc2966`  
		Last Modified: Wed, 02 Jul 2025 04:16:13 GMT  
		Size: 85.4 MB (85355120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251ccd57109451fe7e83952d84b86b2d2c8d7f7038b101b40efff84598d53efc`  
		Last Modified: Wed, 02 Jul 2025 04:16:11 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0dcae7cef67c12eb3c66e5b60363d9a3e16c47993415db2fcf97bddb5fb75462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7594976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855f8a922aa657165c4256c9ae57b0e1ce39e724d468efd2dbb2f63789fd0742`

```dockerfile
```

-	Layers:
	-	`sha256:3d3ddaaf24fe7c4d07a199d60e399fadcb29371c5e5c7c8ed878250a5af4fc3c`  
		Last Modified: Wed, 02 Jul 2025 06:44:12 GMT  
		Size: 7.6 MB (7580763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:481bf4e2692bb87c5217fe3aeb4f95426364d3ab4cddf715e45a314e96bbbf9a`  
		Last Modified: Wed, 02 Jul 2025 06:44:13 GMT  
		Size: 14.2 KB (14213 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.1.1550-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2bfb1746155b63d76f5988afa98128d74fce06d60d85a833298489a359830a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.6 MB (188631385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d84f4d08933a5d04663f2a628ec4403bd9a2d9922511c1ced5125734aee6522`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1751241600'
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
	-	`sha256:2581a046e315a4b3013d50a17da46bcffbba144014a55d733fa55c3bafc6b7ab`  
		Last Modified: Tue, 01 Jul 2025 01:18:05 GMT  
		Size: 49.6 MB (49630154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c321310ff600aca88df94bb71354b12a971bb37d6fdc3c30fae9c4f1afeba41`  
		Last Modified: Tue, 01 Jul 2025 11:59:24 GMT  
		Size: 53.8 MB (53830517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fe0c1ef1caee99e68cc77270728d2d6abdbf74788290314acdc0821e471b70`  
		Last Modified: Tue, 01 Jul 2025 12:04:07 GMT  
		Size: 85.2 MB (85170069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee04c24a8d26ea956f23ae205f6593f00e714cd244d48cc0dab1422fa5a1e10`  
		Last Modified: Tue, 01 Jul 2025 12:03:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:99dd8d5492f9d9b6fbae894d4d051d6480996a6af10b86c05326040a48ffccaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7602822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218ca46a3cc025180e7fcde1d6ec47f3a5e3975aeab7fb97134fd36233eab887`

```dockerfile
```

-	Layers:
	-	`sha256:d47ea98c1083c716c970854db18969091ea3e5f8856b8364b28cd980e00af2c9`  
		Last Modified: Tue, 01 Jul 2025 12:39:55 GMT  
		Size: 7.6 MB (7588491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12d22bb953908535d0262375568ac1f80b7271e1b8149318dc0fdb1cdf9e1b09`  
		Last Modified: Tue, 01 Jul 2025 12:39:56 GMT  
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
