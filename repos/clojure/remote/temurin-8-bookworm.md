## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:0cdbdfea0553cc5323d0917fd8c7dc35eca27c5605d9725751fb93fb5404bb0c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:db1773568bdd7072d77f424d20b5884c2920a106ede16cf6ae649f64852d842c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184361953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab27baeb33a5f43a16724c1272ab20bb4351ec292d97f7429e04d5d08a3fc68b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 22:34:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:34:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:34:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:34:15 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:34:15 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:34:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:34:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:34:30 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf9552cd5b36c1decf1a6aef10f0c9eda43ca6f3542302b7cb7800c8bd49c2a`  
		Last Modified: Thu, 11 Dec 2025 22:34:59 GMT  
		Size: 54.7 MB (54733371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156c0cfe365b768aac49c883757327924c11c2b496f642e1788356f85bdf60db`  
		Last Modified: Thu, 11 Dec 2025 22:35:02 GMT  
		Size: 81.1 MB (81147200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c827fbba1ace5335d4ee3a8edb043afe5b876bccd266edd7f89eb695fe337d5`  
		Last Modified: Thu, 11 Dec 2025 22:34:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:47cf981677b52568c468a76d09e2326374119047788912e3e8a79aa152f7acd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7510693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c21352205e1e7b95b1a0a2f22245acfa4aedd06983ad60e8c90c1f4aabc34d`

```dockerfile
```

-	Layers:
	-	`sha256:cc23ad24ac353cfe05fb02db29e9222fd75e88311b99c574793e0a5ea8b91604`  
		Last Modified: Fri, 12 Dec 2025 01:46:14 GMT  
		Size: 7.5 MB (7496500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9845a78eca95296690524cba895f0473d5b302a37ce430c56a03c89bc2d87626`  
		Last Modified: Fri, 12 Dec 2025 01:46:15 GMT  
		Size: 14.2 KB (14193 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ce727f007d151f15e0d29ad9bc40b92806b6661f4d1c6d656bbda76cb89d690e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.2 MB (183200593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa72cbe3af3a6aa24d16c3582be15007753001a35bcf9497347cf1c0961c9db8`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 22:33:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:33:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:33:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:33:13 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:33:13 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:33:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:33:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:33:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44232e36213234e28eafc3da3366ec91290880f12a1107188882e842dfb8a8d`  
		Last Modified: Thu, 11 Dec 2025 22:33:59 GMT  
		Size: 53.8 MB (53814975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d1c969407b1d569e0c8e0d109aeed0978d2b59a165a38c27454be678b77eee`  
		Last Modified: Thu, 11 Dec 2025 22:34:02 GMT  
		Size: 81.0 MB (81025903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5e7e1294a6d6dd4f9b49931d88a6a111aaa467198fdd55725118f57b59c08c`  
		Last Modified: Thu, 11 Dec 2025 22:33:55 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ffb43361134a1550e38474dcdaa5890c84855b96e0b3d06b5b8d4534892e0118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869f2dabae588bfa0a1dcbac2f2149b184a321c6ed2e194fddb5f229bed69b1d`

```dockerfile
```

-	Layers:
	-	`sha256:308aa245b919975c42e2a62e0f42f16a003ef4e316539a1ab54a179f9b417e80`  
		Last Modified: Fri, 12 Dec 2025 01:46:23 GMT  
		Size: 7.5 MB (7502961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:209aff849ff715e6e0ac793b2fbc254bbf6f3610ac6519747052f942c14ceaac`  
		Last Modified: Fri, 12 Dec 2025 01:46:24 GMT  
		Size: 14.3 KB (14311 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:25d40582968379de1c472dc51f96fbc58c59e50c1fd0cf0de00e155aa916fff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191485252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c87bb7f9b10282f0532dfc911e0efaf1c6ffed8fbcad303aebd25985e5f7ea`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:37:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 22:37:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 22:37:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 22:37:07 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Mon, 08 Dec 2025 22:37:08 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:41:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:41:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:41:53 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a51c77f8794a7a48d981ba475763915c444e47af96f90a51cb42c060ef190d`  
		Last Modified: Mon, 08 Dec 2025 22:38:19 GMT  
		Size: 52.2 MB (52175143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8da3c9f44a86bebe741fa43031da5e83a605fe646319f6d04b5a6253377273`  
		Last Modified: Thu, 11 Dec 2025 22:42:58 GMT  
		Size: 87.0 MB (86982487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3bd45389d99b299000928cabb3c08fd6b9d1d13b38f791843b159c37bc6f9d`  
		Last Modified: Thu, 11 Dec 2025 22:42:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9f4b4c9e6b8e3279445ebdde17bd00bde9837c2f2d9dd32e41420c5558ed27cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7516548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34538d6d88138fcf14f7e325b6385efa8958af20016250a297b2a02e10cec12`

```dockerfile
```

-	Layers:
	-	`sha256:501485a462af1eeb2bcf07f6e06526322f48d94d916920f47128ffa9f6bc1ed0`  
		Last Modified: Fri, 12 Dec 2025 01:46:31 GMT  
		Size: 7.5 MB (7502307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:787ee88e25240773228ae12640e5448f5e8475d24b9c9bbcc7112f641a91210e`  
		Last Modified: Fri, 12 Dec 2025 01:46:32 GMT  
		Size: 14.2 KB (14241 bytes)  
		MIME: application/vnd.in-toto+json
