## `clojure:tools-deps-trixie`

```console
$ docker pull clojure@sha256:3e1c5524a8e12f1adf0a82658606a858f7cd2c6fb87cd5a177a705b440ec5d2f
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

### `clojure:tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:70149514587147f41256513d723cf60c5a48af683751d73782c9deb2762dd582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295089148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f5e8b59904221f4284ead255714a818403a722373abeafd3060d8db9851214`
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
	-	`sha256:8f74611b5dba7cbc5f019083facce00ab400dbe2b351065920462c7d8e1bec20`  
		Last Modified: Mon, 09 Jun 2025 18:56:53 GMT  
		Size: 157.6 MB (157634484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5aa75b07029e7a3bcf721619b7afb3ce852f7a856538a633b4e4a0f641c5cc`  
		Last Modified: Mon, 09 Jun 2025 17:19:19 GMT  
		Size: 88.2 MB (88206713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a512d823b7578b45e28b87a33b6c7514b295ade986e692988e80ab018409f53`  
		Last Modified: Mon, 09 Jun 2025 17:19:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b433ebbd7db913bb58e795f9e49d4e1d1d5102ba586e62d387ab92955e22d343`  
		Last Modified: Mon, 09 Jun 2025 17:19:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0164f9a18cd8f2a380e659dd128d9d21a74a0e111b132a980044cfc04e432d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7478870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48b520aa9bb904b5824befa15286bea172fefcb33ecf5144948c562ae9e27f8`

```dockerfile
```

-	Layers:
	-	`sha256:0d2d1f28075e902a895cc4d9434c0a89d70d8e278013ec9126f6279983dce1ef`  
		Last Modified: Mon, 09 Jun 2025 18:40:10 GMT  
		Size: 7.5 MB (7462405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a36d15b031ac0b52c1bc69df803b35b8ddbbdbd144a52493a7415284a049fe38`  
		Last Modified: Mon, 09 Jun 2025 18:40:11 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2bcc3bca708f6a45d319d0736dc9d1102d888a9d540a21a263b78249d6b7249a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.1 MB (294058913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1567c4c5390636218ab5d10c23e05301c884a1c5d6bc97b7e1b2ea9e089a92`
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
	-	`sha256:669209475ccf588005064aec8b03f795116e849de02f62977a14a87f1ef3e90e`  
		Last Modified: Wed, 04 Jun 2025 11:30:41 GMT  
		Size: 155.9 MB (155928831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874a8cbbc40e5a14834f27ff81176f9ac59f0a77cc90a8d86bfb898c8951daa8`  
		Last Modified: Mon, 09 Jun 2025 17:56:32 GMT  
		Size: 88.5 MB (88510747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8859b47abe90da8b5343cbed330755c3c8b247226f670b902299a33a631fee13`  
		Last Modified: Mon, 09 Jun 2025 17:56:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf3a597e9808f5cac0cd0b776fb75c88ae77c7f242334092cafcd08436776fe`  
		Last Modified: Mon, 09 Jun 2025 17:56:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b5d2d5a3b6af6fee9a32de57a4f215d74e19ab9c4ce6c6797b7727c9101dc01e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ef5a6c0a820252f1007281fde96249689e9d3314e70615367bd0a940b0b785`

```dockerfile
```

-	Layers:
	-	`sha256:43bc8aec5b2c489dbac7bb21bc4764ea920274a52028b5deaa461bf9be86353f`  
		Last Modified: Mon, 09 Jun 2025 18:40:17 GMT  
		Size: 7.5 MB (7469459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffb30620d89090349e8195ad99557bfd8e7e1c946df92f65d9df2d78e70ab91a`  
		Last Modified: Mon, 09 Jun 2025 18:40:18 GMT  
		Size: 16.6 KB (16607 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:e8c14fb75607faef04177ecd34ee4c79276ac3048742fdbb5d5c5f0d960eb950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304836803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ae15a13c2b078849dd427238d3d1331bd9682116ad9e23170ddc91fd4435c5`
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
	-	`sha256:d4f6bd552c8941351aec1fc10e7be3cba78443c32cad3ba1481c6ebefe465a52`  
		Last Modified: Tue, 03 Jun 2025 09:11:02 GMT  
		Size: 157.8 MB (157804856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067448693ed6e7019ab2b94a92bcc4addff5a988aaaadc28ace5af4aba2d6159`  
		Last Modified: Mon, 09 Jun 2025 18:18:15 GMT  
		Size: 94.0 MB (93950363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd5fecd647c0c15914b312b35b51f939d719c1ab1a725612c0d49edfaf41815`  
		Last Modified: Mon, 09 Jun 2025 18:17:55 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edff878010af4646a9f4a5bf78971b850a5dfa5489559c7e20de03fec2dbd8e`  
		Last Modified: Mon, 09 Jun 2025 18:17:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:05cbba753fc1983a0f81be0aa65c663f8544162f60640c13aa9f397b409182e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7483359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153ad46b013072c2811a7117308169bfafddfc881ca5c2bc944145279e8f88c9`

```dockerfile
```

-	Layers:
	-	`sha256:98fc5f2b2fa094e59d205f75e7b352041186659ed4cfeba1d37ab8eb08ed8dde`  
		Last Modified: Mon, 09 Jun 2025 21:38:32 GMT  
		Size: 7.5 MB (7466834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15ee820f4ec76b402ff5d03077277bf12e6a0fcf6fa15345089e1529445da003`  
		Last Modified: Mon, 09 Jun 2025 21:38:33 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:4d7a34179c852594b438246b485d1d84b30711964bca5a43661a2003861c5a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.0 MB (288037360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4e929b5225d4e8299ae6ed1694900212cb88f9048604722612d0eb730a9fb5`
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
	-	`sha256:df655a63a53f1eb7344d055b3a0a02078ae226dc1a077e6b3a1117732b72b764`  
		Last Modified: Tue, 03 Jun 2025 09:38:50 GMT  
		Size: 153.4 MB (153449622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774ac86e11bf8e7d2ec04e7d5b8bff4a8546a1d2a60c25ce6602f3f194106b6b`  
		Last Modified: Mon, 09 Jun 2025 19:15:36 GMT  
		Size: 86.9 MB (86855288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192dabc4532d337695e353a19441c6fffd031334c563ef14082280180e6cf2c4`  
		Last Modified: Mon, 09 Jun 2025 19:15:14 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e65efff2918a54e4dae0f48272d198108dbe43a8eda125c10491836f72ec41`  
		Last Modified: Mon, 09 Jun 2025 19:15:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bb85259b591a26332c2323755dade0f0005fb52316dce82b69292621e10437f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7466853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a01cf8aaed8135def463b6ea10c3e5da4b6e86d0f1d829eed81a09836f4abdc0`

```dockerfile
```

-	Layers:
	-	`sha256:1da978c9d3823995be9c57b97956dfa14ad1f6726fa3b17718b1ffb20eb598f6`  
		Last Modified: Mon, 09 Jun 2025 21:38:39 GMT  
		Size: 7.5 MB (7450328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:301255c83770404a832b79c3df4202d50da4eee3b4d4decbbe50c376b56ce5b5`  
		Last Modified: Mon, 09 Jun 2025 21:38:40 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:5292c4e8a87418afcf3efd881030eaa3467d67ee88c8563cbb6d79d068ad21c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285188453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa30dc9835b1cc8bd43f82de050a88d90da3e5c7de77be10aac60106af7e387`
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
	-	`sha256:861de86bc3adcdc8dc3323ae415856608e017573655a6d8e472b10aef094a90f`  
		Last Modified: Tue, 03 Jun 2025 06:28:03 GMT  
		Size: 146.9 MB (146911014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9171fb7710fb5348edc224f4fca2374b30e55c29d42e3d33ed042e8f719e13db`  
		Last Modified: Mon, 09 Jun 2025 18:56:25 GMT  
		Size: 89.0 MB (88954172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a67af4ec600c67598ed20987c0768697ab699d2d328599d1f802b994676845c`  
		Last Modified: Mon, 09 Jun 2025 18:56:17 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed435631fb60d520f8571a795ff51b1d42ef16909b9c4f28ac7e39d5c775c1f`  
		Last Modified: Mon, 09 Jun 2025 18:56:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e82eaec7da5ac33819a9daa744212a825bc6b185da590b3583da4bb259291fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7474792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45eb3815b40bd0a5f14a7310ae2607b2209fb9782ce17210d5554c64b85ea39c`

```dockerfile
```

-	Layers:
	-	`sha256:8f7c01c3fa6afbb038b78b77045bcbfc9ba8798c5fce530ef7593ccbe361963c`  
		Last Modified: Mon, 09 Jun 2025 21:38:46 GMT  
		Size: 7.5 MB (7458327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f268328abb744cb4cb3dea9ebb351925f1fce8a18c5d9649b0101ed7bcc9c8f6`  
		Last Modified: Mon, 09 Jun 2025 21:38:47 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json
