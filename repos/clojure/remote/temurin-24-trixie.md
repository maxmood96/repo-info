## `clojure:temurin-24-trixie`

```console
$ docker pull clojure@sha256:274609c37d5f5bf2ca268ac0ec2f0bff8bda59918a2632da2addc311980aa7c0
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

### `clojure:temurin-24-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:370547cfcf1ede9c80795f5199802531fe44677c8042905a925a2b71309c22e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.4 MB (227406605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd5f1ea2200ee267513a0ae844612674ea2486dcbdca94c368e10d60f1e2474`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca8130b01352467a2ae4563900dc69157eb0e08a50ec3d6fd6f3709b99e4feb`  
		Last Modified: Mon, 09 Jun 2025 17:19:37 GMT  
		Size: 90.0 MB (89951996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81afbd51f467babee0500e9ba761ffaced1edab50d9192847ee8406e980883cd`  
		Last Modified: Mon, 09 Jun 2025 17:19:37 GMT  
		Size: 88.2 MB (88206660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1f6104780873b0c284e824e3aec11bec89219e98c3d295cd1b1e31a76d9b84`  
		Last Modified: Mon, 09 Jun 2025 17:19:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9e59bc4b56d1a37e4e9599b276c60838db2eb2f6959fcc8b0f5a53db98abe2`  
		Last Modified: Mon, 09 Jun 2025 17:19:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4357a6bb8292e733810ba2d60b3521ec7c6a471fee0e5d5ae2c55bac3849754c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7425070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3823c9a48870bbe527ec61e77aa0cce736385ef480f16ba39c87a5611521d9ac`

```dockerfile
```

-	Layers:
	-	`sha256:8b1001c50474155b62c95f85437fb294965667469b18b7bbdd842661b8715201`  
		Last Modified: Mon, 09 Jun 2025 18:41:53 GMT  
		Size: 7.4 MB (7409281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb5facc91781a4d2750f17b80d73b8e9861481cdd040000186b2cb6f45244596`  
		Last Modified: Mon, 09 Jun 2025 18:41:54 GMT  
		Size: 15.8 KB (15789 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:70a8ea6019ac4c0b8a65dc30ca6284892eb52cf210c1a85622565c5ceabd5bf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227221551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9003b4d7921da7e1179ad079fb4c890dc8c1e6444d21a986dd7cb1bbc31e9365`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Tue, 03 Jun 2025 13:47:15 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7537e79c58dbcab2941c040399879be549690329edde2c0c79c2f4b2c6e312`  
		Last Modified: Fri, 06 Jun 2025 12:15:10 GMT  
		Size: 89.1 MB (89091276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bba0313948318694bf2e813b0a4c677623c80a6a08f37ee813606b178bc6c3b`  
		Last Modified: Mon, 09 Jun 2025 19:18:31 GMT  
		Size: 88.5 MB (88510941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f097a649b6fedd5ef5bd7c36fd07163d0cb683153293721a1b00b10d01b5b3cc`  
		Last Modified: Mon, 09 Jun 2025 18:02:36 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5124a732a3de50007a3cf1b7ed2005bcc153480b46930ded5ed06625c908bf`  
		Last Modified: Mon, 09 Jun 2025 18:02:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b287e421f6527cca22fcea0e3f27f57f38299cd530aec1c6ba53c8abe7fe6b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7432216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d4cba4901a6bf2344770f14526f82121270aaad990d53b30a149f079659b84`

```dockerfile
```

-	Layers:
	-	`sha256:23cb42bdc33fd8c6213f72b59c698f035f26a86b5e8d2947822c1b69763c4001`  
		Last Modified: Mon, 09 Jun 2025 18:42:00 GMT  
		Size: 7.4 MB (7416308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abb7ef354673e9077b32cb6867db2068dbffb5b846975a3b443819e250ddbfef`  
		Last Modified: Mon, 09 Jun 2025 18:42:01 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:dff5626e3db48f02b50221c77d9503281fc7ffa1a6616850ae71ae6e2e59b193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 MB (236952393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2916b3f08ba9b6a1095ea4dce47a2c499e540af051dbe252ba7890b721a8365`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:25dfffa4126a91eb76c700c90bfdc9a9e15f34c7438a81f16c8a6999bbde6e45`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 53.1 MB (53080544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c028c654d0d6c94a628c2a045c90b55cd6b595adae6af5e957fc42510e1de16`  
		Last Modified: Tue, 03 Jun 2025 09:30:35 GMT  
		Size: 89.9 MB (89920265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1850b676671b1f1a9dcb9da53ba3bccc2fe522a6dd2b0e29400c832214b0725d`  
		Last Modified: Mon, 09 Jun 2025 18:26:53 GMT  
		Size: 94.0 MB (93950543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a19264d684821dd9c3de23925822d91a2c397e0af24b00080c8a5e96e405025`  
		Last Modified: Mon, 09 Jun 2025 18:26:40 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095353a677888cd243ca491752eef118c6543f9e87a81eb4288fa1cdbc0b928b`  
		Last Modified: Mon, 09 Jun 2025 18:26:40 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0dd0f1adf79ed0061e9479d182f5e0954442eb464e6633ee014cf678bce37ce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91df6b6a9a5f466bab24327b8dc5d82a2f0c464b7b525e135034d4f1bb93e841`

```dockerfile
```

-	Layers:
	-	`sha256:5897cda6bf5485c25f4913a0aa1cc80bdf3d62157df6bfb09f61057ce20ddc75`  
		Last Modified: Mon, 09 Jun 2025 21:39:58 GMT  
		Size: 7.4 MB (7414996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5566b97eabe7867624b10330862e02bd672c2e1aadbec29109671e7a1beb82bb`  
		Last Modified: Mon, 09 Jun 2025 21:39:59 GMT  
		Size: 15.8 KB (15838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:f4ebeb9701d9e0dc4a25149a2e8ec7d412fdcec356f94cc88d199ed1030c07fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.2 MB (222209860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f1a459b20ccdc0bfe67cda7d30998cce85762f964f1991734759d149d2f511`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c83c5fa20952cc8610d790073e97537e7832127593042fa9c620fa910fe6f6b9`  
		Last Modified: Tue, 03 Jun 2025 15:26:09 GMT  
		Size: 47.7 MB (47731411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e82597a02bb37801e52c801a502f6b2db3f51568e2ab5f847a48db7ffef1519`  
		Last Modified: Tue, 10 Jun 2025 11:59:09 GMT  
		Size: 87.6 MB (87622163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4778f6ca7567cdb7d2dda29c516900fe726a72109bf22ea1838501d57fac8090`  
		Last Modified: Mon, 09 Jun 2025 19:36:06 GMT  
		Size: 86.9 MB (86855240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8da77c2e9f95ec34c99e0863517705d1ce0ecf5c456150349b5bf86a2d4a53d`  
		Last Modified: Mon, 09 Jun 2025 19:35:51 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff24e7295dfa7b3d57c7549715dd79f6fea84801c1fc3cfd6fd920a8b7d2fee6`  
		Last Modified: Mon, 09 Jun 2025 19:35:52 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:107ff023cefc62d645933c14d3700f1d3d5c8c35e8a3b938aba8e4df10409c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7413027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af80e020a5e3d22ec7c4eeea4931548df2cd10257cfc767055448192999f62e4`

```dockerfile
```

-	Layers:
	-	`sha256:3eb33d50819a4fd187b647d958087b3d8472439d2c73abb5265deb28d3da6c87`  
		Last Modified: Mon, 09 Jun 2025 21:40:05 GMT  
		Size: 7.4 MB (7397189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4251b0f21694864c2db8db8b16443697f2f18d251ec1852d5449ad6785421e69`  
		Last Modified: Mon, 09 Jun 2025 21:40:06 GMT  
		Size: 15.8 KB (15838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:8782940928c4b2b4a89dce1620191b2c417719d961356b34ea3b03f28b7760d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.5 MB (223495379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2104aa8c3871afa322cfc70b52bb8bbd6f637714453fd2dd05d576db6820dbbe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71c8524b25c34592c256fbae9045d0ade48f5e9889d37c5b2190092fa9017d48`  
		Last Modified: Tue, 03 Jun 2025 15:34:07 GMT  
		Size: 49.3 MB (49322227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d2065613a1620d7fd64270b68c955b617708425a53d56a91b8997efdf6f3fb`  
		Last Modified: Wed, 04 Jun 2025 11:30:58 GMT  
		Size: 85.2 MB (85216756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20270c288a40a5b81220b8bbcdedd17ef95b9143a0d4c364c732590b00610757`  
		Last Modified: Mon, 09 Jun 2025 19:01:11 GMT  
		Size: 89.0 MB (88955354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfc752053dfc802d8d8ba397b86c7c328a56c7f46e072eadf3c3bf4486834d6`  
		Last Modified: Mon, 09 Jun 2025 19:00:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8098f5bcc2fcb9af8fd0a375a585135514704dc6c60cb4b6c7040b5a9c8083`  
		Last Modified: Mon, 09 Jun 2025 19:00:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:54216d388dc6ac1817f4561d3c2abd142769b2da7ad47c5930b98176e1281f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7423541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7b74822582178b9cc47bbef36ef83be6da95e6a6691ba9eb3720065dfdf817`

```dockerfile
```

-	Layers:
	-	`sha256:7850a04c9ef52ac3dbf3e621c6b6c00af2adc7448f65fbfbde35d7cf249d6395`  
		Last Modified: Mon, 09 Jun 2025 21:40:12 GMT  
		Size: 7.4 MB (7407751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b5c7fd9c7cdd71b1296e94b1f9e9955291fae6c93a53964c309afa4c2550dc6`  
		Last Modified: Mon, 09 Jun 2025 21:40:13 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json
