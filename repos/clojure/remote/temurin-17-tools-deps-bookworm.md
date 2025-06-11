## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:740e073646a72366a3ba8e9c480a224c9415a2d72912f2fbbd2899e68d4835ca
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

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:bcb5ed0344c918b3094dd5a46f2a6e8a5cb8be03371d086587981aa1a203a9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274124349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd56110d58f5176ac5ea129cc2f7c2189c14546eba7138e51354455b1ae1cde`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1815a20fd7a32d4bbf42a0603242e9fa4e6ada340432d1812eae3181d47643a8`  
		Last Modified: Wed, 11 Jun 2025 04:06:11 GMT  
		Size: 144.6 MB (144635025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53bd0f12a0becebd2cb722211a2444441dcdf4aada04c4a14e6aa1976f7ddcd1`  
		Last Modified: Tue, 10 Jun 2025 23:52:18 GMT  
		Size: 81.0 MB (80994010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b1b5635587c7ffe9c799483b5b16eb0d983022fb093b6d328e63fad226a585`  
		Last Modified: Tue, 10 Jun 2025 23:52:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48de59967b033128f645a91d5c6383ae88cd64f1157ec61fd2f28ac51b98114`  
		Last Modified: Tue, 10 Jun 2025 23:52:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:edcaa7a3b3099dfcc1a22f3c3dfc48f9d873c8bd970ce8aee96def4a04e8cacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7382733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d9285b0856381a72b037de3f2d3b879fc940719deff0370e76e4df6ed73f17`

```dockerfile
```

-	Layers:
	-	`sha256:fa9d3e81ec1e4696182c2d5b907d4eb875bbbd7edcc99443748b728638ceed27`  
		Last Modified: Wed, 11 Jun 2025 03:36:35 GMT  
		Size: 7.4 MB (7366912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91aa7ce2cbd2e758817d888a33b4ebad790553643bd58b193848c308757521b3`  
		Last Modified: Wed, 11 Jun 2025 03:36:36 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d03684f183ea2ba9d8e2dcc579feec03bfbbb7dfa9520ab7b1c912dc95cd6969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272701259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38ce7eae363fe19eca97a206ec83a6ec5cf41c7ad8b85507f02a19918c82f9e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63bfbd0e8254ebcfeb8c130af328be36cfb0ef9e0e10b1979b6cb2e14c5e410`  
		Last Modified: Wed, 11 Jun 2025 08:24:04 GMT  
		Size: 143.5 MB (143512635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1493a0093f3f93740462f87cb3aafdc87598ee07a95ce280025c8443b5c208f1`  
		Last Modified: Wed, 11 Jun 2025 08:29:57 GMT  
		Size: 80.8 MB (80848732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b5a12a3d8cad316071eb338b43f1d958582d4c435afcc84e7a5a017e30999a`  
		Last Modified: Wed, 11 Jun 2025 08:29:49 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5274e712a07035c378ac815fbcb869de87f632f394a1cfa197253c72d28eff`  
		Last Modified: Wed, 11 Jun 2025 08:29:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:109a76931bff1db78761096d620125b623d67adefb1110b1aa03a11421c3e4a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0287691cff8a5412feecbc1596054fa12458bc620a084cf86b29745d6da039c`

```dockerfile
```

-	Layers:
	-	`sha256:8edbc43bdf505bd5ae6faccd7eaee2e104fe5a6cbb7a2efb8c6f151323132e03`  
		Last Modified: Wed, 11 Jun 2025 09:37:19 GMT  
		Size: 7.4 MB (7372675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e3df1b66b9740b1bc321d27b56f637491d4bfc2d567e523fdfb8d3acaef7cad`  
		Last Modified: Wed, 11 Jun 2025 09:37:20 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:fc4a110795006c66173fe31e323d7ce763f28f951861aa403316c4cfac6c79f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283432553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119822f4784cf622a40821824d37b1b5fcc577f4785fec042698b3734094f078`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:65d348c3abfb8493d4b77022d58f0afc8e2daa19b2af853f803aef5c836212f9`  
		Last Modified: Tue, 10 Jun 2025 23:28:11 GMT  
		Size: 52.3 MB (52337357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9b1c2d893c980cf722a4786a9033764d9c55166784c4fcd2e21651f8614b7e`  
		Last Modified: Wed, 11 Jun 2025 08:25:57 GMT  
		Size: 144.3 MB (144280582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fcc52e22b457e85b9d85f0616e0e6c504d7099c5ca6c20903ab9e7e932e0cc7`  
		Last Modified: Wed, 11 Jun 2025 08:33:46 GMT  
		Size: 86.8 MB (86813569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911b7cacd00e75f7db048aac56296864243fa1c25cfda4f62721e1cdc9b311c8`  
		Last Modified: Wed, 11 Jun 2025 08:33:23 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38b1d3c1d26cc4f7af92553f145ec9cc6045c1f84fe863011d219a1ff92140e`  
		Last Modified: Wed, 11 Jun 2025 08:33:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ac45ecd9b89381d0b97eb045add2fe6694d5abb3932e3b2c71c65d6348d307d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7387985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257cda5d827ef953e39503683983a45d94d9da8e22fdfc8d8cc7f180ea1bf73d`

```dockerfile
```

-	Layers:
	-	`sha256:1d10debb423b52ec5299b1e31825ac9f6e5f8bb24c353ea596553ef83aaba775`  
		Last Modified: Wed, 11 Jun 2025 09:37:26 GMT  
		Size: 7.4 MB (7372116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75457afc855b4653a8b9040565d54c91a26daebf0ce101df3a787fabe21e2b0`  
		Last Modified: Wed, 11 Jun 2025 09:37:27 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:86c7c608f66bf8c335463a6725bdb688dcf742f43b91ed6ba882ad768a66ef0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261626360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a92dea2122dbf3e0f235251c0e62f343a530f278679bcfaeed59b8e8164d42`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
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
	-	`sha256:92d876c60c42d9677caf30587cba2266fe6860ddc50efdd0a6fcec154e589f76`  
		Last Modified: Tue, 10 Jun 2025 22:48:13 GMT  
		Size: 47.1 MB (47149408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4543e40eb732d0ccb173aba0b476a19947bdf35993df6b756ce3ddd02191e16`  
		Last Modified: Wed, 11 Jun 2025 05:41:34 GMT  
		Size: 134.7 MB (134673550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04e5044f10e4c2b2cc05490982884933f4368349bb15d18973e6912a48486cf`  
		Last Modified: Wed, 11 Jun 2025 05:46:01 GMT  
		Size: 79.8 MB (79802362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce1ac3f86dbbb92049f6f52ff248eb8a9781cd45c8db4af1da4de1c8f36e4cb`  
		Last Modified: Wed, 11 Jun 2025 05:54:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69e007142ac4eae156c03aef71de3251aa4481684c19b91ba0b248b02df503c`  
		Last Modified: Wed, 11 Jun 2025 05:54:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5e4dd0f89b9daf56fce36bcbdb857e695dcd69b3c1ded27a8ff77e75b2aa0d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7374052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56df10fda5684dfcc801b4104ab3f4a6505fcb25376cdd6552275e66cd35a2d3`

```dockerfile
```

-	Layers:
	-	`sha256:fedecda2bc5ed5ec6b3ae2552ad510d400d6b1d10b4c1cc9f6cfade35aee2027`  
		Last Modified: Wed, 11 Jun 2025 06:36:21 GMT  
		Size: 7.4 MB (7358231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:477ff6e01f9848910b28c8e64ddc221b448ff0038153f0524fa9ef8c64660ce8`  
		Last Modified: Wed, 11 Jun 2025 06:36:21 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json
