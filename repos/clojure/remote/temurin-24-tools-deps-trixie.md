## `clojure:temurin-24-tools-deps-trixie`

```console
$ docker pull clojure@sha256:4577a9f29c3c89e55d98db9d5fbbd48d2f636d14d2ef67ac32e49110703665a6
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

### `clojure:temurin-24-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:a7fb172344b1cff5bbf97f9309f8643017fba5bc32698299671fbd61a4f43088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.4 MB (227422673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6136b1f4ed917593b9cf0f0a7494bc94038c5e7df368029d3bd1bb673591fb1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f8f138bedeec141ce3d55ce0b45f1201bf4586387cff12a9796b55a032bbf8`  
		Last Modified: Tue, 03 Jun 2025 05:17:08 GMT  
		Size: 90.0 MB (89952019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e738ca0291c9237a916711717d6e8bc714e3d1a4e4515a59c73ac7b6564835`  
		Last Modified: Tue, 03 Jun 2025 05:17:07 GMT  
		Size: 88.2 MB (88222708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f6c8b8cef156ded1a8319e2f5c44cd6b50b5ec21d85811d10dd7303196e35e`  
		Last Modified: Tue, 03 Jun 2025 05:17:05 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb27a1147660d6fa3320d0cee5fbe6f62a68c9084886a6f3e1853e277f63cc7`  
		Last Modified: Tue, 03 Jun 2025 05:17:05 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4b4d1d594d579dde1af876c098b98d7fe17e64b65d7cf7a079a138bb68696a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7284851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b7e43498fb15be1d231c991720e03083a676ee7822d6ff83469019061b0e23e`

```dockerfile
```

-	Layers:
	-	`sha256:d6ed041a9e4dadbc5544dbad36b599c61610b260c6c3b52e2852a1a223b2d946`  
		Last Modified: Tue, 03 Jun 2025 05:17:05 GMT  
		Size: 7.3 MB (7269062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7a0fd86ebf0a8757bdcabd1bb00493d7a47a712c226686931a93b6dad9fbba1`  
		Last Modified: Tue, 03 Jun 2025 05:17:05 GMT  
		Size: 15.8 KB (15789 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:498f7fc1e042ff88f027b46716e7347c73d47c0c5f50092bb598556a300c8e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227216658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:febfd3529ebe5397f9c0921f53ef04405ed4d899c1faf994acc41ccda37c11a1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Tue, 03 Jun 2025 13:47:15 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7537e79c58dbcab2941c040399879be549690329edde2c0c79c2f4b2c6e312`  
		Last Modified: Tue, 03 Jun 2025 11:09:31 GMT  
		Size: 89.1 MB (89091276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc66eb36bf7d80517ca827f4780d8f9b58a3f3ba006a319fad30248b67bf7c7`  
		Last Modified: Tue, 03 Jun 2025 11:16:22 GMT  
		Size: 88.5 MB (88506050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c49d9e70489145772f944796684d901d11e534be036e0aefa1dbf52a2dd924`  
		Last Modified: Tue, 03 Jun 2025 11:16:19 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87db0629e1d1bdb45c388a839ff2d1b9269c210e265d9b92f609e028f927cc9f`  
		Last Modified: Tue, 03 Jun 2025 11:16:19 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ad3d723f2226100ada5d47323c4a3da8e0be0db9e05a1a969b2ad8d1a252a97d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7291997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc2008ffd49b42563813e54b2f530f978e4f23b09af3c2ef0c1e9c6b235abd98`

```dockerfile
```

-	Layers:
	-	`sha256:8b9b83e754330e1282b1339adb3f0a510ceddec8a3447a3ed695cb31ccac644e`  
		Last Modified: Tue, 03 Jun 2025 11:16:20 GMT  
		Size: 7.3 MB (7276089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3dea0965dcec35ad4e4a26fb394c872bd1f803104b2d8e2366c1680e3b3da67`  
		Last Modified: Tue, 03 Jun 2025 11:16:19 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:96665018ecfbb3fa1f8feebf1df077ba516f02e5ec42d7f1fd26f74ca985045a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 MB (236958541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9945225192200c0bca9746d85b92d8abc8a1c4750c905919f3491d9e754834d4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:25dfffa4126a91eb76c700c90bfdc9a9e15f34c7438a81f16c8a6999bbde6e45`  
		Last Modified: Wed, 21 May 2025 22:32:01 GMT  
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
	-	`sha256:4468a6ea44aa8858c4474fcdfb08648ae91ef48836420638f58927abaadb338a`  
		Last Modified: Tue, 03 Jun 2025 09:39:50 GMT  
		Size: 94.0 MB (93956691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345fe04d748873b8ab54ffb34a67ad41ae9c1779d56a89b37cf128c738cdf8c0`  
		Last Modified: Tue, 03 Jun 2025 09:39:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7da04bc930b8cc8b6ffed5659f8f9245cc4e1593f0031c3681cdb88dca9606`  
		Last Modified: Tue, 03 Jun 2025 09:39:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d002efb4a0d3cc63a7095ff76b814da4368b701e5879d442866cf05e6b58619f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7290614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46d41b8f986000fa0860627f5f49adba7df92c14f3928dfae5025e717ed0e0e`

```dockerfile
```

-	Layers:
	-	`sha256:a5570e4ad8923bf49c59bbe5382f18dbda63df72260126f5e07d336c6a3b2eb1`  
		Last Modified: Tue, 03 Jun 2025 09:39:47 GMT  
		Size: 7.3 MB (7274777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11b757a197d9008507ff1da25357e43f6509a842d4329196c76ef42feea1ee1a`  
		Last Modified: Tue, 03 Jun 2025 09:39:46 GMT  
		Size: 15.8 KB (15837 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:0e49bd01bc0d8357bfe495ab096f9f53275319a80293c2a1f7b2ff219999c824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.2 MB (222195412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bed312e020673e97858e01965544996247bc96404ed16057ee46682985e910`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c83c5fa20952cc8610d790073e97537e7832127593042fa9c620fa910fe6f6b9`  
		Last Modified: Wed, 21 May 2025 22:36:51 GMT  
		Size: 47.7 MB (47731411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e82597a02bb37801e52c801a502f6b2db3f51568e2ab5f847a48db7ffef1519`  
		Last Modified: Tue, 03 Jun 2025 10:22:55 GMT  
		Size: 87.6 MB (87622163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1fce9db642b0666713d055b07ce95299624beea2534fedae084333154644cc`  
		Last Modified: Tue, 03 Jun 2025 10:44:17 GMT  
		Size: 86.8 MB (86840798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27b4f20df423da047e8345e9cccdb7b5faa0a23efe2e6a0edcd48fdc539cc33`  
		Last Modified: Tue, 03 Jun 2025 10:44:05 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431c2898ef2742244c745c02efdf1a53815cc9e72cf30ea2fc0079c969ae7ce6`  
		Last Modified: Tue, 03 Jun 2025 10:44:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1cd744f531d220bca39ed8f17c67cadd4768ac3fc01b19801dc43a1344c9a549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7272807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a2af0186039b93442c0fe838ba388ec3c7fd38f30448a000eb54fb95930710a`

```dockerfile
```

-	Layers:
	-	`sha256:86f51900fe15033b3cf954031850399eae1b63bc19e4badee55f7e361fa5788b`  
		Last Modified: Tue, 03 Jun 2025 10:44:06 GMT  
		Size: 7.3 MB (7256970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b27d95b8a72b8797e8ef155fdd4acd8908b1c6ac16ca6cc64342a1d0c448766`  
		Last Modified: Tue, 03 Jun 2025 10:44:05 GMT  
		Size: 15.8 KB (15837 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:4486f33c4739b8077a804ee6575dc024bbca4ec02a40f04d7752c6b0f395f973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.5 MB (223491166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0f6a3586f1cb9b51d93e948f096434a4e940ac321fd8739afce68f6aa6732b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71c8524b25c34592c256fbae9045d0ade48f5e9889d37c5b2190092fa9017d48`  
		Last Modified: Wed, 21 May 2025 22:31:46 GMT  
		Size: 49.3 MB (49322227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d2065613a1620d7fd64270b68c955b617708425a53d56a91b8997efdf6f3fb`  
		Last Modified: Tue, 03 Jun 2025 06:38:49 GMT  
		Size: 85.2 MB (85216756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecddaaa2456d69b0fd7775a2146de51ae2767c148712c06f6556678da87d611`  
		Last Modified: Tue, 03 Jun 2025 06:43:43 GMT  
		Size: 89.0 MB (88951141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e6bd8caee19add41b842ba2b25c2ca76ae851b17cf55af0a673f5c825d3143`  
		Last Modified: Tue, 03 Jun 2025 06:43:41 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98de768dc31c713853290c86171ecfc842b7f0b6c14fcabe464a2524e43b107`  
		Last Modified: Tue, 03 Jun 2025 06:43:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bb4f80d1c8617311e205b259795a1e1a48b3902c9d50943f53f496b821b7faaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7283322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689d95dfb933d39bf6ccc8ba8dbaf5b370bf3951747515a8f2406aa70194e9c9`

```dockerfile
```

-	Layers:
	-	`sha256:bf542b06200fbcd211f626d638ce709fd280c7b7e144d106e274ce647a237714`  
		Last Modified: Tue, 03 Jun 2025 06:43:41 GMT  
		Size: 7.3 MB (7267532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9903fd5c4c14c8618a12086a50b6d7466580d2be98c0b71037db2eb628ae9995`  
		Last Modified: Tue, 03 Jun 2025 06:43:41 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json
