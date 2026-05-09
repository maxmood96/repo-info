## `clojure:temurin-11-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:179f0c966c09c0b3a7d7f35a32c1fa6ba95fa071640d9bda4b00bdacd2006c8e
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

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:84b78c10b807f4a568ea1f64c0eaae99807667406b1167b12a2237eaf4b38312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247678194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa6b35c8bbfc59d71720d82ca9daa7aed59a79f94edaefd515ae189b8c35889c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:16:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:16:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:16:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:16:23 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:16:23 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:16:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:16:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:16:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f061f925025d14a6ba997857d4ce40a616b71a9bf54d99399599a76b22df61`  
		Last Modified: Fri, 08 May 2026 20:17:02 GMT  
		Size: 145.9 MB (145886200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96fdfa74f063439de9ec1a9b6d67a71a0a1fa88668a0abc88f7fda12202f5d5`  
		Last Modified: Fri, 08 May 2026 20:17:00 GMT  
		Size: 72.0 MB (72011122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf06d94d687c84c930e231933d372b39355033e0f612b86c0457327c325a20d2`  
		Last Modified: Fri, 08 May 2026 20:16:57 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3b7c71d4ace3881d904712b38f30284aef97a806b35abf398163ad9a0a39cfd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f15744bca2b19ed12e12c521da6da23aa5feb81065c11b8caac7f4f0e607a4b`

```dockerfile
```

-	Layers:
	-	`sha256:420cf0ccef8093b0bc898738ae0799a205ec72d15ca5676912ef7037df90930c`  
		Last Modified: Fri, 08 May 2026 20:16:57 GMT  
		Size: 5.3 MB (5279335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74ef45c812df3a9595f72a8a39819ce17ef47330f08a065b7e049ac5a56f6bba`  
		Last Modified: Fri, 08 May 2026 20:16:57 GMT  
		Size: 14.4 KB (14397 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6e772d9dc5ca9132c8a1a88be68f909bcd1ce5b3a3076978c036486b3707de90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244558205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b9f004f23fdd64aaef8495a994e14ab83c03e844a5e97013c77701062b57a0`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:20:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:20:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:20:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:20:43 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:20:43 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:21:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:21:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:21:13 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f926a7f0cc937a9226b5f1cb7cc6096de2e86823db882fbdb49bb25717d7ba`  
		Last Modified: Fri, 08 May 2026 20:21:39 GMT  
		Size: 142.6 MB (142582234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7857b9abc27317746d06eaf0e0dc592e19ab79781f53c646876f8c5f5aebcbd`  
		Last Modified: Fri, 08 May 2026 20:21:34 GMT  
		Size: 71.8 MB (71831684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4152d787deda2883265c5ca7adb3243fc23699135296ec114700d4622800c2`  
		Last Modified: Fri, 08 May 2026 20:21:31 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:19e4817cebfeefa5d4fbd91928dbde08f14d4e0dcb1a3a6495b3a9a4fe3a018a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5300237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338bb720b34926f1cb2418e227f1147b26716cf79a28d5ab703bc4059facbd26`

```dockerfile
```

-	Layers:
	-	`sha256:94144329ff313915fdb704d0f32844d12758aa34cdf671d50a5e2dab2c2cd6d9`  
		Last Modified: Fri, 08 May 2026 20:21:31 GMT  
		Size: 5.3 MB (5285722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9994f6d5776f333f35a5b3bdba0afa7827ac971cad43a1a5a9677fc2ab52456a`  
		Last Modified: Fri, 08 May 2026 20:21:30 GMT  
		Size: 14.5 KB (14515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:dcfb21999e7ba31644f31601b2999f817a28636849795507e0eb2a469b29f6af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244137588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d86123234c2274b48b35fc4669eabac1aa401da320a5f451c36610cdd18c0f`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:26:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:26:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:26:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:26:45 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 09 May 2026 02:26:45 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:29:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 09 May 2026 02:29:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 09 May 2026 02:29:57 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96ee5b4d347c9b3ee6f86dcde18c044f7ee128c0ca544845fafbcc3bad0c1c3`  
		Last Modified: Sat, 09 May 2026 02:27:49 GMT  
		Size: 133.1 MB (133110179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f7f00d8f3385ea2b3133c22675be05e9f667085ede76f1dd88c4dcc89e06bc`  
		Last Modified: Sat, 09 May 2026 02:30:29 GMT  
		Size: 77.4 MB (77428674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886e91079d47f6b6c5598e427e2303f224279ff734d21ae5a2b62230a86e068a`  
		Last Modified: Sat, 09 May 2026 02:30:27 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f222200246d5ac98d8bdbc8c27b8c514e9887720cd1464e6b8c57545542bda28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2ef247f05e59c3c3a6be72955d437c5190846d3922821c5f1711543fc106b4`

```dockerfile
```

-	Layers:
	-	`sha256:9e5a8d7cebe62da100ce45e1809dcd7005566c7704c7aea66d9217476880983c`  
		Last Modified: Sat, 09 May 2026 02:30:27 GMT  
		Size: 5.3 MB (5283091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:948b71a4e9c3a39f06b790f5e092a42d8efb263ed31995a7f0fa00528b38ad8a`  
		Last Modified: Sat, 09 May 2026 02:30:26 GMT  
		Size: 14.4 KB (14444 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c4c4dff4027110769bdede4edc98e939612d1f7a8fcbeaeb7e8b4b3e0ed04af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229479554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdd5cf97e0ea10885af910c0587289e053ce15cac783403be0012ef856b49524`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:13:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:13:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:13:50 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 22:13:50 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:15:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 22:15:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 22:15:02 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f616beb9fa3f85be0df9ff578c65c04793648f333a4daf9843ed26118d89ab38`  
		Last Modified: Fri, 08 May 2026 22:14:29 GMT  
		Size: 126.7 MB (126651715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c1ac163f38028cf633ca4230e4d70e62f22f92af4b8e86fdc07369fb27dd54`  
		Last Modified: Fri, 08 May 2026 22:15:26 GMT  
		Size: 73.0 MB (72986847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f1d15db580c510b6532edc8e4ea9db6cfa2f54725912699801fef66af7eb2f`  
		Last Modified: Fri, 08 May 2026 22:15:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9e46d0e06059b71366137da548e7db4d0ce7cfcd4faf2db38114527d7124fc4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5288704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2215dd194d5d31440cc483e229ba6b33cea7c20ea4a2f982b09b548c9e10f181`

```dockerfile
```

-	Layers:
	-	`sha256:fa38305d1692263923db6b20c0027175fc9c9d9b88e270eb627fbbb99c57147e`  
		Last Modified: Fri, 08 May 2026 22:15:25 GMT  
		Size: 5.3 MB (5275263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21597ff6e0c829e5adcf62e56bfa6b2bc448cb2e6814ab37ab81bba374db5ff1`  
		Last Modified: Fri, 08 May 2026 22:15:25 GMT  
		Size: 13.4 KB (13441 bytes)  
		MIME: application/vnd.in-toto+json
