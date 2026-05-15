## `clojure:temurin-25-tools-deps-1.12.5.1638-bookworm`

```console
$ docker pull clojure@sha256:c197b000ad2f8775897227b6dc074065a794f71083a85ce6ca8421d5c1c37e15
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

### `clojure:temurin-25-tools-deps-1.12.5.1638-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:79e115543b753ae0a78f54f76a20db3dca134817ab18eeb1bb56c902f340448d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.3 MB (222278293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c74e703766595f2535dda1c6dbedb436f3eeb8cc82ebbb207344106804e43829`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:33:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:33:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:33:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:33:15 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:33:15 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:36:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:16 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bcdc8504277ffc1c492da7bdd0db99a4d4cb73d300397c02367164c22915c4`  
		Last Modified: Thu, 14 May 2026 23:34:07 GMT  
		Size: 92.6 MB (92574586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5826226813bd35111d371ab4a0767ee463d8b6e0dd506cea2fb51b152a8b36e3`  
		Last Modified: Thu, 14 May 2026 23:36:34 GMT  
		Size: 81.2 MB (81213988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d9fcb22b664000e57d863778b86ba22d0417f3c7f0917e756e121931613fd7`  
		Last Modified: Thu, 14 May 2026 23:36:32 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65cf40c5e0bef0bfcf4ab50fd8ef7c1c3adac88b883f3ac28fa5a1d2efac1ff4`  
		Last Modified: Thu, 14 May 2026 23:36:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1638-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:33e13291883598650bb6237becc9e399269ef6df036371eaf6c6e05449ab526f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7366246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133bc47eb905a62d97dc119c1e470503efdc4dedeeeedbdefb7fc8b34b92daa0`

```dockerfile
```

-	Layers:
	-	`sha256:8ceb59e2eabfb1099304be124aa1736b2028afb88086fd9ba514d869642d6219`  
		Last Modified: Thu, 14 May 2026 23:36:32 GMT  
		Size: 7.3 MB (7348321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f236c2a457ed622de027dc8db8166090dc72474ccb0e57bd3a8018b96df79d5`  
		Last Modified: Thu, 14 May 2026 23:36:32 GMT  
		Size: 17.9 KB (17925 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.5.1638-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ce184e76583fe0c4fc171efc148ade814fbce6c0cc90955686cf9f21e13d0442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221112384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1725922b53f457f71470c083ae4a21803574c4de1ef4ad8636b9da973dac698f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:36:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:36:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:36:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:36:08 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:36:09 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:36:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:24 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3553237e65edb332e9fbb4b659704086a487db7bd28301d0b05f17938dfb726d`  
		Last Modified: Thu, 14 May 2026 23:36:46 GMT  
		Size: 91.5 MB (91542246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ca5525577ee140afd2336fc639e6f61a5875bd001043bbde9b375190dfef0c`  
		Last Modified: Thu, 14 May 2026 23:36:46 GMT  
		Size: 81.2 MB (81195944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841ffcfc06ea69a714aef89e7bdfe7607d3ebcf3b8148655f12d17c9d3616585`  
		Last Modified: Thu, 14 May 2026 23:36:43 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97242deeaa94a1c187b53db3ffa662c8a0b49c485e31c25ee67c21c74beb0440`  
		Last Modified: Thu, 14 May 2026 23:36:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1638-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:40b400a780d9ac2858448d33cd5e8ee3b9286dbd90ff526b432e9021925910ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7372267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d80afc94607cae999b2827e462850e53103df4c88e925986d07541529115b1`

```dockerfile
```

-	Layers:
	-	`sha256:a7e506d540a354f6eef1d4698968fad551902dc16f83d9f4d4035505c90029c6`  
		Last Modified: Thu, 14 May 2026 23:36:43 GMT  
		Size: 7.4 MB (7354153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7301f3ca88b5a888099d419117f0000f482776cf2d8469065f5a499fc78121a2`  
		Last Modified: Thu, 14 May 2026 23:36:43 GMT  
		Size: 18.1 KB (18114 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.5.1638-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:f5ac67ed1b562c5c9f297312ffdc6bbd6842e3ab2aaa2d1f4848d55d97afe2ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231285038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73ada0883a520dde17ecc7b9638598cd773d76e5ec9a65334be44206a4347dd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:18:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:18:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:18:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:18:51 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Sat, 09 May 2026 02:18:51 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:51:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:51:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:51:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:51:47 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:51:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5de956b7a11284f1a158aa4d174299365ba072baa5eadc5c41d537c7ba7509c`  
		Last Modified: Sat, 09 May 2026 02:20:31 GMT  
		Size: 91.9 MB (91914029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1620ae80bf6e621998e3c688931d618238b525cbc6707457c3bcdf5075a4c8a`  
		Last Modified: Thu, 14 May 2026 23:52:26 GMT  
		Size: 87.0 MB (87033173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a425a8df9d151eb4b5ba1d55329e6a21de885b3ce13b37df621650fd8571fd`  
		Last Modified: Thu, 14 May 2026 23:52:24 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f09874cdaeee78e252b29db66976b6298cc8210764033dbed3eb34d2139151`  
		Last Modified: Thu, 14 May 2026 23:52:24 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1638-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8d7ffeb79e634a4edf8c8e9840e477954b8d60e505fad733b5e0eceb05479db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7353941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce306d18f4b2c1fbc010cd2214cc6b9ed18061fa43d7343482ab340fc46490a`

```dockerfile
```

-	Layers:
	-	`sha256:e38edf7b15acc27906b34ead131ab22c8bca314962e7d514ee5371266dd9d39a`  
		Last Modified: Thu, 14 May 2026 23:52:24 GMT  
		Size: 7.3 MB (7336885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eefbe32b189b4c736d2303d198282758a67813caaa065b9fc460250b2fdfd383`  
		Last Modified: Thu, 14 May 2026 23:52:24 GMT  
		Size: 17.1 KB (17056 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.5.1638-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:07758131d27482901b845c793c19e5a6c2ec6bc740220f0fc5631b2c60b295c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.6 MB (215594374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de7534f51056e155f021d6c7b062f1e415eaa8bebe52accd8d2a00e745101ba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:37:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:37:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:37:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:37:14 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:37:14 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:37:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:37:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:37:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:37:27 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:37:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919ff6944cfdfe171e630be33be41e61c43d3607140de9849e84caf428ea01ef`  
		Last Modified: Thu, 14 May 2026 23:37:55 GMT  
		Size: 88.4 MB (88420336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfac6d67bd478e253145ec858bf3e036fa8974aef034f4b84928d267bef1b94e`  
		Last Modified: Thu, 14 May 2026 23:37:54 GMT  
		Size: 80.0 MB (80024969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2c1be02183290c8f76aa6caa5d76fb866bacb22f056f67a6500a120db39266`  
		Last Modified: Thu, 14 May 2026 23:37:52 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46202d966d42e3cf91c1c7c35013f54b3c2ff28d0bb447e7455938e98c4ab02d`  
		Last Modified: Thu, 14 May 2026 23:37:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1638-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:86e955ee4a20086bfa41e33bc0a3157a8725fbac6482cd77b1a4e16529db594c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7342127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094f6ca9322f4a8f454e25e9f8a2ed4e8a105b385ccf41d314244b4e1b10e47d`

```dockerfile
```

-	Layers:
	-	`sha256:1b076b337f30f20689611f050c39d14787bfb1190e947c958c657f5abc98923a`  
		Last Modified: Thu, 14 May 2026 23:37:52 GMT  
		Size: 7.3 MB (7324202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3b65959e6ab2300647bcc1a58d4df001648e2dd56320a2db6740f59a020fc0c`  
		Last Modified: Thu, 14 May 2026 23:37:52 GMT  
		Size: 17.9 KB (17925 bytes)  
		MIME: application/vnd.in-toto+json
