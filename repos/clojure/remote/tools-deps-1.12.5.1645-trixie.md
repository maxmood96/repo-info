## `clojure:tools-deps-1.12.5.1645-trixie`

```console
$ docker pull clojure@sha256:ac8b6ae1c00ace8fb804bb1d693d32c609ed7087ad202781e9bb6a8946cba155
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

### `clojure:tools-deps-1.12.5.1645-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:fcdc53557b9c221fa8c75c789e8b7c7d96a322efa0cdbca8b1fd28271357e574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227481488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e34913f2d5a9e244459b8731bc8b68fd7de1e8cb479309d64aee2eb43ecadd19`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:16:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:16:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:16:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:16:10 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:16:10 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:16:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:16:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:16:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:16:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:16:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012b166ac5adafce01ad3e58a07b9d3c7fe050f19bd742b5c9e2299c775bc0ac`  
		Last Modified: Fri, 15 May 2026 20:16:49 GMT  
		Size: 92.6 MB (92574589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385801ca07d21c19cb2c6e80fae8b86e47aef62926733a99a77e4fee511b3511`  
		Last Modified: Fri, 15 May 2026 20:16:52 GMT  
		Size: 85.6 MB (85603537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39802efcd3c5c47d45ac0891763d03e5193246fa35c94baeee014a19d1fc249`  
		Last Modified: Fri, 15 May 2026 20:16:44 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b09360e82c7bd08e3d823e26e4413a296e5d97a41ceba53c8925265f17b87b`  
		Last Modified: Fri, 15 May 2026 20:16:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1645-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4975f87102740f5cc943c4cd6c6581098df7f99a2481805e9542f335788228ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7456013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d755d6d5555478cc76157ce8b780ef94c5bb2cc4dfd8241318180ec2b0d1a49`

```dockerfile
```

-	Layers:
	-	`sha256:9a16e0fd8d2bc2d9458c6a2fad397df1782376c43cc6e164042b51768eba0f9d`  
		Last Modified: Fri, 15 May 2026 20:16:45 GMT  
		Size: 7.4 MB (7439444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:806d56aa3fcd04e6675ee15e1cb6616811889650ecd2b409a0397e508fc9bdcd`  
		Last Modified: Fri, 15 May 2026 20:16:44 GMT  
		Size: 16.6 KB (16569 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.5.1645-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ccd4d8e29d01acd13c9a9a9cf7be7c3c77ca2898380660705f4d0cb0b38083f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226628154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de11384bf173ef60dd838e3f15559b46b8718b1031d1552ffe89b716e56015d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:16:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:16:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:16:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:16:13 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:16:13 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:16:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:16:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:16:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:16:31 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:16:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a585bc135b4a7328b968a7e3ea6be7e3de0a30a835beb50e7136cf297de6c3`  
		Last Modified: Fri, 15 May 2026 20:16:55 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb20b1ad8544deccfd1f8733615fb5c357c6823df48ffc40d4376e989a6fc4a6`  
		Last Modified: Fri, 15 May 2026 20:16:55 GMT  
		Size: 85.4 MB (85415413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442bcfc4e41d9c84dc6aced5ee267ec87725aafcb24a6408ff0da6ae2e309932`  
		Last Modified: Fri, 15 May 2026 20:16:50 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859fa332166d6ed8f8fb37c654557551904985c8f1db4b208f5b4bea38539817`  
		Last Modified: Fri, 15 May 2026 20:16:50 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1645-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:607766a76f55611355285b4372dd8cefb2285b8b550790e1f985117312266924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7463206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eeae80a4c1b72e73387cfc2f0ca726bf15c62de5c85ea32b08df4a82d19c764`

```dockerfile
```

-	Layers:
	-	`sha256:d27d6f7b7dd1bad2a8ac96227fff63fffcd47ddc993cc153e93632a04b0efb75`  
		Last Modified: Fri, 15 May 2026 20:16:50 GMT  
		Size: 7.4 MB (7446495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8773b35ad58d1bc82c7b3b3f1e9a1689aa1b9c1c5c4c08f590c2bf89eb2b197d`  
		Last Modified: Fri, 15 May 2026 20:16:49 GMT  
		Size: 16.7 KB (16711 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.5.1645-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:08a0695799b395a768ddbc748511274d8264a8c0f4e5f0a24f9421b1bcc7c8fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (236045826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4003875a2d5854371d03842ad3117567208ff69e8341744536b3da60c6c9d08c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:42:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:42:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:42:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:42:40 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:42:40 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:33:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:33:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:33:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:33:46 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:33:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2325345b811e94f6ff3ccd6a646a97c3cc4365dd97daee1fdfcb79b03cec8cfc`  
		Last Modified: Sat, 09 May 2026 02:43:51 GMT  
		Size: 91.9 MB (91914029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9883aef0bc85acd55be92f3be8d783a164545c8b39a214d255c516dc194c0214`  
		Last Modified: Fri, 15 May 2026 20:34:30 GMT  
		Size: 91.0 MB (91007585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5471725dcc8234aba5a0046f06d6ff2617c22849010ff89228bd5870caf867`  
		Last Modified: Fri, 15 May 2026 20:34:27 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40576b25892aec4cf9a8a5f85de9be6fdaf3701cb0e8504ea535d9a3508720c8`  
		Last Modified: Fri, 15 May 2026 20:34:27 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1645-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:258b9e5d7df25663f85cfd99f920a113a30c8ce4fbd7b3ab4e69e684d4e51d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7442863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c15a3a0d78e771e9decc5baf1e1fa47c6f063ed21a2bdc39f3ca7d89f11184`

```dockerfile
```

-	Layers:
	-	`sha256:0ad9849b65f58c43ab8ae4a4435c10f16faa51910d1f66583f308de5eb46b0ac`  
		Last Modified: Fri, 15 May 2026 20:34:27 GMT  
		Size: 7.4 MB (7427189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18476ac61778607fc2da3bad89670b6ea9320272c552d8e8a510d9b446d2fa4f`  
		Last Modified: Fri, 15 May 2026 20:34:27 GMT  
		Size: 15.7 KB (15674 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.5.1645-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:b63e06a120709b4dbf2590f29b7fca821de551802dcb15abc4b077051661b883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.4 MB (224360131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b0d461501c5025b66f7e69bd8613c50a7cbe92df3ccac4c91b93c770d55ef2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:34:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:34:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:34:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:34:58 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:34:59 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:37:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:37:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:37:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:37:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:37:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a92a76ae7b655491f20639c1a27895a4fe7338273ae814b1de259101697f0c`  
		Last Modified: Fri, 15 May 2026 20:38:16 GMT  
		Size: 88.4 MB (88420336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291de378db9c19667d00b6f891370a8c84be230b97e3589f787d6241f62b2d6e`  
		Last Modified: Fri, 15 May 2026 20:38:15 GMT  
		Size: 86.6 MB (86566445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63597033dfd787e9ef0392df547a1abf1a5ee472ab426cac41d5951259c063b5`  
		Last Modified: Fri, 15 May 2026 20:38:11 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5857ed32944d53d5be9f432168f2c9d6c92ef34db0dd94e7fc44fe86c7d96e93`  
		Last Modified: Fri, 15 May 2026 20:38:10 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1645-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:edfd80599b15b9caeed2945ddade79a33895bb9ec4eb44557fd5f0e3c01d3f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7436497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cedab147490d65c65fc906d8b9059b5839f410fc8d942f249413efdd4a8fdf8`

```dockerfile
```

-	Layers:
	-	`sha256:9fe23aeecc6c6a2659d6d45b0776d80287c576fcf8e2ad04528cb74d027b9ef3`  
		Last Modified: Fri, 15 May 2026 20:38:11 GMT  
		Size: 7.4 MB (7419928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a666fdb1043f4ad254f58d5ecc1e371db9f3ba7128d5aa76ab04405b673340e`  
		Last Modified: Fri, 15 May 2026 20:38:11 GMT  
		Size: 16.6 KB (16569 bytes)  
		MIME: application/vnd.in-toto+json
