## `clojure:temurin-11-tools-deps-trixie`

```console
$ docker pull clojure@sha256:49a471724b0680d4dc786e7b56486b09ccf118a7af4948dcd9b3cb59c65f4bbd
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

### `clojure:temurin-11-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:092cffdaf2045603cd6919c56bbfbbfbdbc75ad69fcea321e297b90dd609020e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280471501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2dca654a1789e601a3b59f2cdfe6a1b98e7298cac692407b7b25f0600a225e4`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dfec0a94b76810a218fe17a8af420fac087da290a27e9ae9adc13e477ab638`  
		Last Modified: Mon, 08 Sep 2025 21:42:48 GMT  
		Size: 145.7 MB (145658209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252c26cf4d6470769fbed8e388f7cfe7bcdc9ff03c7b9715c28287a47d42d615`  
		Last Modified: Mon, 08 Sep 2025 21:42:52 GMT  
		Size: 85.5 MB (85533117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d186006e9550c7ad00d71fd4f9e27159567d85ae8e278e6ac784ec5a57120be`  
		Last Modified: Mon, 08 Sep 2025 23:03:56 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:07b0d06d08d544670d00128c1106585e66abd48a9a08caa1c7c96b832e0e4084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7501213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8022ea18fcd1079ad3fdd9b9784ad118f8fb6cd9bc4190b5da25fbfb14ca98d8`

```dockerfile
```

-	Layers:
	-	`sha256:7f2bd82c587a34b8bb80fab3d957f982cab3fc3b949427e0976a6a2a030f4c75`  
		Last Modified: Tue, 09 Sep 2025 00:36:56 GMT  
		Size: 7.5 MB (7486986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:974483a0bcfb4e481cd38898343a8dd39857299e75c0a72f002fad2c6cb136f5`  
		Last Modified: Tue, 09 Sep 2025 00:36:57 GMT  
		Size: 14.2 KB (14227 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:151cd1b6cf4c17a877730741e2135c273a5f118203ebb8ecdccda7fa6e0dd3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277461510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9648ecbea84f933fef69f640e83be1c1c9e9fe1107afe561532adc220f7c42b9`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01cab2d5f1e1ccec1c96586f23cc634b2495a459c0782e41f2d3d6c7025248a`  
		Last Modified: Tue, 09 Sep 2025 00:38:06 GMT  
		Size: 142.5 MB (142459120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa6bd838c45ab8e781379f4a75daeae95783a0a49b8f8e0989f88953259c7c2`  
		Last Modified: Tue, 09 Sep 2025 00:38:05 GMT  
		Size: 85.4 MB (85358000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e3d7839e9f3e2428e5cfd232efdec35e52864590b46da587022cba31261fc6`  
		Last Modified: Tue, 09 Sep 2025 01:27:53 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6d04d9cd05138ae4c21b0f9b510cc2b845c0a61ba146e803f9e3ec3dc7dd701e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7508980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08bd146c39d3490478828cfc7d61e173260dc46be8b0bdf6df89e3af4849dcc6`

```dockerfile
```

-	Layers:
	-	`sha256:9878c659317efb89b21a57c25b543efa9fd1c8118bb27c77da70112af8379584`  
		Last Modified: Tue, 09 Sep 2025 03:36:50 GMT  
		Size: 7.5 MB (7494634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:225eaedf45c131a37ca549d05cdc0170fbc5a2b7833dfbe262b1f80a9744667a`  
		Last Modified: Tue, 09 Sep 2025 03:36:51 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:85118b79c68cd8f77085ad52df3e447a9d190c4dc3a5b226d7c1bb26bca10b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.9 MB (276898770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe8740c633c09624cac90cfaf56e02c3767b3117ed5c26e2b751e836889d0d3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d59d569015f70604fe51fcd56c3b07ce6b7dd5197efeeb62cd5cb7f57c9bd69`  
		Last Modified: Tue, 02 Sep 2025 08:16:55 GMT  
		Size: 132.9 MB (132853128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab89079b2660190ff7b5a4a123c6bf158ad58739e4ada6275ad2954a10cfd488`  
		Last Modified: Tue, 02 Sep 2025 08:27:02 GMT  
		Size: 90.9 MB (90941611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d543610e3716285b813f4ef7832f0faca80fd553246c46f865268641c0d608`  
		Last Modified: Tue, 02 Sep 2025 09:16:04 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:25b2caa73e4ba7aeda9a5196d795c9028e08e1a5a6973ec4c49e5fec90ae99e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7500442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb1679c8bab73b1061a8848eab9d57b2b0adaede12f9c72726f77a4b0c99c12`

```dockerfile
```

-	Layers:
	-	`sha256:ce479f615a63822e55803ae551895a63b065ced4559ad3f3673bc2c212980f5d`  
		Last Modified: Tue, 02 Sep 2025 09:37:29 GMT  
		Size: 7.5 MB (7486166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d60cc28be9c43f5d3180e02d8ce065257c2ffb4862d50a1aec7f9354efee40a`  
		Last Modified: Tue, 02 Sep 2025 09:37:30 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:2d0cbf34e5f90575cbbe0144e833d0a24aca0120c5c07c60f0c9fbcd186105b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261475426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06c2245c109b34ed1e4489c56974e69f72dcdfd879a4ab276384cbe1edc581c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:28eee642962fd09c10ecf87da2d4b65d208f3d5c1bf3fcca21c105c0213f558a`  
		Last Modified: Mon, 08 Sep 2025 21:32:18 GMT  
		Size: 49.3 MB (49346327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5c173fc2633ad8afcf6f0979f77c1c1c0dfe739ebf741748b555be75bac538`  
		Last Modified: Tue, 09 Sep 2025 05:29:30 GMT  
		Size: 125.6 MB (125622199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad12592f95cd4fe1afb9b9759ca14e541bdb7c8813cac0abae1051e049952de`  
		Last Modified: Tue, 09 Sep 2025 05:32:29 GMT  
		Size: 86.5 MB (86506256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7689bad2a44a7b3f6561a28af23692dedecbc46dedbd5f71bf8c32eae58c3121`  
		Last Modified: Tue, 09 Sep 2025 06:11:49 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f7891642515f53aa21cb9c2acadf6262a616db998b715bf47ce3fa8289ed8c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7497140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de9ccab21d3be5956e4a1ada5099ede02bbbbeb696832075b0ffb6a6dd019de4`

```dockerfile
```

-	Layers:
	-	`sha256:7c058975629c9a06133a9156176ed147ba199e59acc9b22df58d990ea205fa49`  
		Last Modified: Tue, 09 Sep 2025 06:36:20 GMT  
		Size: 7.5 MB (7482912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae6940fda2aee536615ddcd179084fbfa5a8b6d16315b664db220a44429e2030`  
		Last Modified: Tue, 09 Sep 2025 06:36:21 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json
