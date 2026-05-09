## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:e41b7b42ba9edfc0cbdff4e403606f02500287f09a03efce505efd35713d4336
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

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:754085b8120fd01375e434cfad1448a63c02757a661b7ee2d5b5314dba1323ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256103320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfa4257183966df63effca4a077a2b9b0999d7e5587bcd8172588e0a546932d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:18:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:18:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:18:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:18:14 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:18:14 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:18:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:18:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:18:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:18:28 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:18:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728a0bf2e3131fe7d05e71eb4648a91d0f147d06a1d728024d0552a8db758bf8`  
		Last Modified: Fri, 08 May 2026 20:18:54 GMT  
		Size: 158.2 MB (158166935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d979aa529c3c1f5ef306d149e28fe99352d3f859fdb48ad0418bd30ef39604da`  
		Last Modified: Fri, 08 May 2026 20:18:51 GMT  
		Size: 69.7 MB (69699061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabce49b5463263c1b1a95cf26acafd848ac1c9e73ef82e8632f88703dcbc9dc`  
		Last Modified: Fri, 08 May 2026 20:18:47 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4598d95fd76a04057380b4f8cf406e8dc3ae5f2c254d0ebf588371ba2c33164e`  
		Last Modified: Fri, 08 May 2026 20:18:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a2cd04cc48d8cae5642ae617844c5b98419b6b8b5c3bd5ee1f0b1b2276cb38ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f315ddea0b390417a4c515ee761b3587e4a59ee6ba3d7a99b61e5ba0fed8ef0`

```dockerfile
```

-	Layers:
	-	`sha256:c165cdc5eeba7311990f161e0f7bb526baba368e6a35c8d9b8f4399200a636d0`  
		Last Modified: Fri, 08 May 2026 20:18:47 GMT  
		Size: 5.1 MB (5118646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4fb034c1e60d3c6f5ba109b2b6cb0e0821dddb7da05cbe0337ff69e127b99d0`  
		Last Modified: Fri, 08 May 2026 20:18:47 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a2706fecc342c348954e3e2697dc52fb0809cffe243d3d9f46478fb02e56d191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254271005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8974f90486357023318963142b93abe859c86c026e91d781f78104b7adc72601`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:22:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:22:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:22:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:22:47 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:22:47 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:23:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:23:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:23:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:23:01 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:23:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e26d0fbe90cf12ac24181a520a7b37307ff4e61b7be0063559bb734ac030585`  
		Last Modified: Fri, 08 May 2026 20:23:24 GMT  
		Size: 156.5 MB (156461225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec02c89224045ee22f4d904eae114ab0654c25f967a78faf84cc5f5b68d6cd76`  
		Last Modified: Fri, 08 May 2026 20:23:23 GMT  
		Size: 69.7 MB (69692574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8a5256982423bcce8b2fad7c31ab45c7f6f218f1b0c8cf663510cdfc3b7470`  
		Last Modified: Fri, 08 May 2026 20:23:20 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82403f35f152762e1fc23bfe2c8ae77bc061443c0944198d8a63921bbdb4d49a`  
		Last Modified: Fri, 08 May 2026 20:23:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:30f209d6fe1d71afac2fb4b49d61ed15378fb69f5dd41423b989d7d730fe74ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5140515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d34ac8d5cbb4cc54e044263d5cce3e6f6599b6c99b0efc2ccc0c4089ca47e7`

```dockerfile
```

-	Layers:
	-	`sha256:a317b1429b77cdf871202f9c6131fa7fb6ce271d493de895c118ab5663d061c3`  
		Last Modified: Fri, 08 May 2026 20:23:20 GMT  
		Size: 5.1 MB (5124407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cedc237f0d107263137e312db621d31cd7291c516d7b67056d69319e1fcaa7e`  
		Last Modified: Fri, 08 May 2026 20:23:20 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:1e9123a6b885b78c31f9a6e35306b730a6d183035667c74b4ab31e57c91fc981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.0 MB (265952770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de7cc32a19718fa0110f41b2d42c1b20d0d88a86bb2beab295ceb689cca9f56`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:36:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:36:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:36:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:36:33 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 09 May 2026 02:36:33 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:39:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 09 May 2026 02:40:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 09 May 2026 02:40:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 09 May 2026 02:40:00 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 09 May 2026 02:40:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa7fc9485b4fb59cd58fcb71fcd4db3dba936648eb297bdcd72a79d669b2338`  
		Last Modified: Sat, 09 May 2026 02:37:42 GMT  
		Size: 158.3 MB (158343237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00722a6fcd88c54b3cb32ea5ee81453acec4b7129dbc14db0bc4f8911cb10954`  
		Last Modified: Sat, 09 May 2026 02:40:35 GMT  
		Size: 75.5 MB (75530040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106ec4ee0358766f03f20bd98371000eb23f441b79981956f3d8f0ea4dac76b8`  
		Last Modified: Sat, 09 May 2026 02:40:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1099079766c46acce2164ab47196216a424585d052a59c2de17d77ceb1739889`  
		Last Modified: Sat, 09 May 2026 02:40:33 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1a359d46d1eac5fbba44c324974c8fc62e7deb1560c6d0c5a02efee3fa3db43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7762233170c8df198d30e64f413c727b28be57897db467e35025a888f0f229b0`

```dockerfile
```

-	Layers:
	-	`sha256:de599408fcb8902141de4076cbf5b4435a48ad54ec083b6aaa92b8b2de49845f`  
		Last Modified: Sat, 09 May 2026 02:40:33 GMT  
		Size: 5.1 MB (5123804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02417fe811dfbbd2fc617661e09e1f7b29740a8a3f52e57445b80d84a0b3bbac`  
		Last Modified: Sat, 09 May 2026 02:40:33 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:82cc108fe6b3b5eae4b9ad47a4a805c72a0dcef91bd44fb7d7eadf2fd3ea2d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242793581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f142a9a2b7c9ccc6f2311dbefbee5a94c5d2c030f3f4a8b06594c978d26f4c8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:16:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:16:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:16:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:16:57 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 22:16:57 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:18:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 22:18:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 22:18:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:18:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:18:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9927e4ebf9213259a4ef5a3246c16010c9dc3952f2cdaf14171591311e8b7dc5`  
		Last Modified: Fri, 08 May 2026 22:17:39 GMT  
		Size: 147.4 MB (147388334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8043337ece137a61142b276a421e2eab7d6aec0a3dfe38711f5eee50112206`  
		Last Modified: Fri, 08 May 2026 22:18:34 GMT  
		Size: 68.5 MB (68512603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5476e9e170c7b47cc8d18376c70c8562aadd02b557d479abfab544c9fe5fc1a1`  
		Last Modified: Fri, 08 May 2026 22:18:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a4bd538b55e4c702816611e8eb792a8c43ff0ca85b702698508be114bad336`  
		Last Modified: Fri, 08 May 2026 22:18:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:efe58628cf6e71847121a556806f49fb0c7618434b6a92ce44f307f2840ea460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d14d2926a8ed2f7e73755865c682d53260ff87337e323c11435563d0828b6d`

```dockerfile
```

-	Layers:
	-	`sha256:c827672c1900bb671ac21ac2144ae0d993418f155d6d76662f4eb0277e3f26fd`  
		Last Modified: Fri, 08 May 2026 22:18:33 GMT  
		Size: 5.1 MB (5109967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:269a8fb3b523666201ba55564366a50fc09a5a17b5cd466e5ead0f9a737792d7`  
		Last Modified: Fri, 08 May 2026 22:18:33 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json
