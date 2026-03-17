## `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm`

```console
$ docker pull clojure@sha256:bd7dcd17692f20c0ed08d429c8b7620adb1142e78038ab1a4e3c73f3075787cc
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

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:a8f0c1e4077016001250906c8ab51bcb749ab51616b71aa714291898e5a60c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275473379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1b04e0b75c4fe3695323319b4be092d31da524ad0ac29655f1b7af4051103e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:57:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:57:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:57:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:57:18 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:57:18 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:57:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 02:57:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 02:57:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9d947a4ddbd004f6a81a71f1e541b7a2b5349b44a91e343ce419d5c46bd7d2`  
		Last Modified: Tue, 17 Mar 2026 02:57:55 GMT  
		Size: 145.8 MB (145806912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37904e02e0d9fc1dda8d34082b13f4fddd5b11c8f0e1d63e7d6365b4a88e3c5f`  
		Last Modified: Tue, 17 Mar 2026 02:58:00 GMT  
		Size: 81.2 MB (81177238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d02b3e8ba4c5804efa98a98bb2faead5b1c646bf1568c7f564af234ed4e80f`  
		Last Modified: Tue, 17 Mar 2026 02:57:57 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2c790c97f5f82f20af42c69977402b32e99b410a354c65781e01dae740ef66f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7412652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652b5e7f6dcb36457d9ea22938ee4a306c664ac33a99447e3384bcf7c045665a`

```dockerfile
```

-	Layers:
	-	`sha256:744a5c3f7766f0a54759d73d1fb43314dd2e9a2d08b2dc58581a7da822b3cb32`  
		Last Modified: Tue, 17 Mar 2026 02:57:57 GMT  
		Size: 7.4 MB (7398443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18fd2424bb839e01232f9f01959f134f06f5289b4be7609b2705689779e60684`  
		Last Modified: Tue, 17 Mar 2026 02:57:57 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:45cc589d3736d35e75bef8cfd5717b9569b12cc7a32733239aeebaf737fb202d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (272032061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74cbf090d219aaace26b18d638ed34faa3aaa97e4852c0e747499426e3190503`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 03:01:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:01:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:01:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:01:50 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:01:50 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:02:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:02:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:02:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bad337430304e6581e9cd2ea833d27c5521ce94738307e3d500f4962138bfd`  
		Last Modified: Tue, 17 Mar 2026 03:02:29 GMT  
		Size: 142.5 MB (142500050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2187f4814b1ab36cffc556b50a0b29a1d194c5789b99385ca288683f77ce22`  
		Last Modified: Tue, 17 Mar 2026 03:02:28 GMT  
		Size: 81.2 MB (81158336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202073a776faf98f67b4eb847aeb73341c8e76eb10e2d702729ee37354e915c5`  
		Last Modified: Tue, 17 Mar 2026 03:02:25 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d5e16dd0b3662c258b5d2b51898a09fe37faed42593ae43775c82c1cf0aab303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b913baa09d3cb6967a8b7a93d5d85994a1674be5fe195db737a0f11f56faf39`

```dockerfile
```

-	Layers:
	-	`sha256:64656219aafc9e2f10e46ecaf52eb862a20ac2ff61c5d1d402ad8894045277ec`  
		Last Modified: Tue, 17 Mar 2026 03:02:25 GMT  
		Size: 7.4 MB (7404824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6bb96914d23978f65e486ba5fc38ea155b90f307c79a6df0805cfdde12b8512`  
		Last Modified: Tue, 17 Mar 2026 03:02:25 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:6fe193a0f68ae9e6bb9afd10521f8e14953f489edebda52f8d2ca3d88f3aab92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272334171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5711e0d6349cd22833e654d9d4016e604ce375c79f5a1abff11dd09d4bcc7e09`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:15:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:15:41 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:15:42 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:20:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:20:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:20:49 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c072e92b832614e86d956c6381c6b7617944feae3193ea5691e9506870844136`  
		Last Modified: Mon, 16 Mar 2026 21:51:19 GMT  
		Size: 52.3 MB (52336698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbecbf7ecf5689b9ec9a2fb7833196c9e479474539bbea61e477b10fa3c1a715`  
		Last Modified: Tue, 17 Mar 2026 18:17:05 GMT  
		Size: 133.0 MB (132996700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be671bba964e222550568c709017ea34bf00ad187b011426ef729f2058c5d8f`  
		Last Modified: Tue, 17 Mar 2026 18:21:29 GMT  
		Size: 87.0 MB (87000129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195551047080f5e747289317b95caac03f79ab8c8ff94f15d57a3e5f8a6bef5f`  
		Last Modified: Tue, 17 Mar 2026 18:21:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:abb4668bc0dababe5131336afbe221966abbbd96de112ff798fc858641d581f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7417301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b58e10dffcf6683f7a31369d1f3e1b96fc5f5f17da7566799d6e6753641e39a7`

```dockerfile
```

-	Layers:
	-	`sha256:69e2984996075424fea7a6b33e8eaad5b650a7823143e43f8a915c61593494e5`  
		Last Modified: Tue, 17 Mar 2026 18:21:27 GMT  
		Size: 7.4 MB (7403044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4633d921cdad0f6d3e596f76035fbd08f71f5c8435af9df311d211cf0280ceee`  
		Last Modified: Tue, 17 Mar 2026 18:21:26 GMT  
		Size: 14.3 KB (14257 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:43a23fdf40239fb4f561c8870c3b2e8b594012d918a35ddd04e1ca50537ba9ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253699229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc97dc19ebe695f79677689f2a88393dce68c520807745669a7a320bb61a1b53`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 11:26:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:26:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:26:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:26:27 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 11:26:27 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 11:31:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 11:31:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 11:31:09 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7dbc3949555449666cc7651209b926019d3fc7f1511f7ebcd8979762b12d59c1`  
		Last Modified: Mon, 16 Mar 2026 21:51:27 GMT  
		Size: 47.1 MB (47147919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9613fb1a68bb280e83d2b60c4423035c2328571d1d7d4f2dde5aad40c8474713`  
		Last Modified: Tue, 17 Mar 2026 11:28:40 GMT  
		Size: 126.6 MB (126562115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38502097938777d9c1e559a662d424cfff38222b727312ea17c97bd6a3b69f45`  
		Last Modified: Tue, 17 Mar 2026 11:31:56 GMT  
		Size: 80.0 MB (79988551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dca142985635e1308e8dadca28ed2c8d755f8bbd4e681ea59bffb82b4b746ac`  
		Last Modified: Tue, 17 Mar 2026 11:31:53 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f6d7161da74e122e8a770fca327d8f41f2df39e690d6cfd5d89a9db46537316b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69ccacbbfcd593437aa0bb345ef2c9efee370292cfd401b8a8369320f201378`

```dockerfile
```

-	Layers:
	-	`sha256:51865967f4883559e4c0b5c34bb4d0455e31f3f2562a73e2917368ed6d38f06f`  
		Last Modified: Tue, 17 Mar 2026 11:31:54 GMT  
		Size: 7.4 MB (7389766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed064e5690219e915773ca23a533b1e7b57a3317187541bc3967db1e9659c99c`  
		Last Modified: Tue, 17 Mar 2026 11:31:52 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json
