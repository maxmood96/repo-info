## `clojure:temurin-17-tools-deps-1.12.5.1654-trixie`

```console
$ docker pull clojure@sha256:96dd9a1fa4fed6cc3f91a67803884a7d9cbd79b8b6b274d4bc7848bc9dd4c6c1
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

### `clojure:temurin-17-tools-deps-1.12.5.1654-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:734da98ad98dbf7c484bcd9a5ec1be5a523aa453cee9e268e994a885e9875637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277742719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80c17acf258b81ddbf8989a76ba8a30089c238c2279bf5ab1fa67e0df5e7d1e0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:17:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:17:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:17:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:17:54 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:17:54 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:18:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:18:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:18:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:18:09 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:18:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240bbc47a198ff249bf12450b6d59c2c534d89fb7642e3042dcd6d6a2d25ca55`  
		Last Modified: Fri, 19 Jun 2026 02:18:30 GMT  
		Size: 145.9 MB (145905437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7616ceeac3ee7509f4d0b3c96c24758eb4ce01fac36e94b06d3c11e449e3fe8`  
		Last Modified: Fri, 19 Jun 2026 02:18:29 GMT  
		Size: 82.5 MB (82519124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d178c34d75576382c4d4c3a503c1489918f070b583046730ce18d4bfbf6607a`  
		Last Modified: Fri, 19 Jun 2026 02:18:26 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5f589f4d6c38bf02d6a47eac433783bc684c522d99f0acf374526f8785eee4`  
		Last Modified: Fri, 19 Jun 2026 02:18:26 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:73c69bb6d862c0390f5588b8319cb809b9d6db8c8f3d3c1d18ee7d436c4e00c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7484679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a8a7f1350367ec50a80d7fab5e7e25a816620dbbbe155c7514b5946dd8ce76`

```dockerfile
```

-	Layers:
	-	`sha256:e0490ce8b1c69be1f0bbe41c3aaaef9a4437ccb1cdddef8798027c3a6a109ebe`  
		Last Modified: Fri, 19 Jun 2026 02:18:26 GMT  
		Size: 7.5 MB (7468771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10c893b6245e93a5d6bbdab24e380e3868bffa3ef6120b54756270b9892ea5d1`  
		Last Modified: Fri, 19 Jun 2026 02:18:26 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1654-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f4d6f795da328190fef7af2c33dadc0d83bbb9f652ca17514c63990d5dc1e562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276742132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa442ad508319743491e7eba83705994b373d7312be11903c6ea1af7badff69`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:18:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:18:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:18:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:18:16 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:18:16 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:18:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:18:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:18:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:18:33 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:18:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727f7dbe8e4fb209103709e4e8e3007a9c8bffe27dc89d51b3a3882a5d474363`  
		Last Modified: Fri, 19 Jun 2026 02:18:56 GMT  
		Size: 144.7 MB (144724318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0eb1b05cbd64143a089180c25f132354ba5480b20a6fa901defc2a3667414c8`  
		Last Modified: Fri, 19 Jun 2026 02:18:55 GMT  
		Size: 82.3 MB (82338603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e96ad56d41b2078bd984c2767597b3a169437f1600a1debb4d3c1975192f7a6`  
		Last Modified: Fri, 19 Jun 2026 02:18:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15434afb5735413dfb5b2e328df4344018d66c90a184d671ead53652a47ebda`  
		Last Modified: Fri, 19 Jun 2026 02:18:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:075e2cf54d94b1104a9bca9185bb1dcc4d8ec505ed13ea2ca90a5a6cb75fb2d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feadd9bf75b9b1be02baf4ecec878de6244f1d198a28834f19b5bfc764902eb2`

```dockerfile
```

-	Layers:
	-	`sha256:0742b5264f9b2c24f659b88040fbda1ae8f05828449dff700d3219569d70a384`  
		Last Modified: Fri, 19 Jun 2026 02:18:52 GMT  
		Size: 7.5 MB (7475164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d08bf62612b7d74b4d2f39e9116098a3e29e3642ac43a11f3d87aa51dd08d47`  
		Last Modified: Fri, 19 Jun 2026 02:18:51 GMT  
		Size: 16.0 KB (16023 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1654-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:26baeeeb339bc69845650ba5d3610002dfde546903ada227514bed8a11b4a865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.8 MB (286843976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcbf7413f55737cc77eddf9ef2a793e2a554566008ce4a769239eabb09257968`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:40:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:40:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:40:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:40:48 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:40:48 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:47:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:47:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:47:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:47:55 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:47:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4c522651359f2b9382194c5170132137b32f6d0214c41d2c39ba3ec770a8cb`  
		Last Modified: Fri, 19 Jun 2026 02:44:52 GMT  
		Size: 145.8 MB (145766191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551b2ca7bea8aa0d149a7d6228c220d1eb850ee641b23637f13e04830a40c77c`  
		Last Modified: Fri, 19 Jun 2026 02:48:40 GMT  
		Size: 87.9 MB (87938802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b3454e3eaff6273defe4e9a36538923faa7f811f684f93b558dc0889314606`  
		Last Modified: Fri, 19 Jun 2026 02:48:37 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6910d7560d0c4ae727068e2a104771515e2db7f19f7fc6cedea6c337ffb4d26a`  
		Last Modified: Fri, 19 Jun 2026 02:48:37 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6def1c7ea772ce8b8d9fea59c48307e95cc623a53a7a3fe00e6ffe8d5217f1cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42e454e0b123f6e97584b1be586a62d62fe399332b43a1b7f702f58800750b2`

```dockerfile
```

-	Layers:
	-	`sha256:785f0214d5aa4f9d10b2d6ebfd93d47c33ec9af565bcf769f2d036d131af9d42`  
		Last Modified: Fri, 19 Jun 2026 02:48:38 GMT  
		Size: 7.5 MB (7473192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54ff817eecdcfcd4f7d518eb86a8e5fdc893266072bfad062a2dad6bd5372f08`  
		Last Modified: Fri, 19 Jun 2026 02:48:37 GMT  
		Size: 16.0 KB (15956 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1654-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:951b2f0d094ce462a3b714212a1c7eaae93fca152d3e89260b744f6a211307e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268799232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a780cefff3c6738a7f572ba1b854dec85c3ad026c3f034185dd0bbea9e80153`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:17:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:17:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:17:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:17:08 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:17:08 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:19:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:19:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:19:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:19:14 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:19:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918861cf680bf2b5b17504c84afdec10f9b09d3eb5a7a38387c5b5ff00597b16`  
		Last Modified: Fri, 19 Jun 2026 02:18:42 GMT  
		Size: 135.9 MB (135910421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05604fd093201395c35e0a394ebb9ffa94b07b9257b46627be968776477205b`  
		Last Modified: Fri, 19 Jun 2026 02:19:41 GMT  
		Size: 83.5 MB (83501876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249c0659418bbd4736ff737df8293b75fc22336f9507bb51e569117737922763`  
		Last Modified: Fri, 19 Jun 2026 02:19:39 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a4181474c5ac99a9bd1948edfb4952a4f76073c22102f8cedd3d77cca6dad0`  
		Last Modified: Fri, 19 Jun 2026 02:19:39 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e9d5e27d40d28f4ef56570ea433e392ffab25d919b6c3fa12b9d1d2d0182fb29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7480601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e8d245d18e3cf3f0f1ca0f546053255784a12a2f6ce5d75cfa89d975a5d172`

```dockerfile
```

-	Layers:
	-	`sha256:562a8b19a3761ceaf411909f1c9224e7c382dda9ad7efb37807b75e5ede2cb8c`  
		Last Modified: Fri, 19 Jun 2026 02:19:40 GMT  
		Size: 7.5 MB (7464693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:008fa772681810b0ff09b1b2dd4a5d6255eef2a8a173a110d04a93c21a1e3449`  
		Last Modified: Fri, 19 Jun 2026 02:19:39 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json
