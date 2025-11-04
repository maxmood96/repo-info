## `clojure:temurin-11-tools-deps-1.12.3.1577-trixie`

```console
$ docker pull clojure@sha256:44eacc024e45d6c55948f05ee89ea59b614e6576d50ec06a7cb46548eca3b6ed
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

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:c60c940399a97bfc9601d57b51e8dd7c030d8be932b966bca2b05b7e19c1dcd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280484870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1557b29901820cfff3eeb30a81d2bee650e8897f4c63b1ffde9e5ee41078c36`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:30:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 04:30:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 04:30:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:30:34 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 04:30:34 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 04:30:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 04:30:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 04:30:51 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5188a818dfa0a0c3d15344613e4a2b523b26e717682ffb03e97d7d2608d90308`  
		Last Modified: Tue, 04 Nov 2025 04:31:15 GMT  
		Size: 145.7 MB (145658332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed3ca27b4033050d4d775c70f34f6997681898acb6365b0f661ed34314dd5ec`  
		Last Modified: Tue, 04 Nov 2025 04:31:32 GMT  
		Size: 85.5 MB (85540266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca57000a28a50654816890be379bd2440abaa71f7600848a4eb87b9a6c18740`  
		Last Modified: Tue, 04 Nov 2025 04:31:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b2f43f77eef3780a7ce062d7b5d33d856bf73431f697138377a8a20aaafc3678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7501224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc81522a9768b984fd3ffcb7081d561a0184f74e090e3dacc1ac6b5e09dfb0f`

```dockerfile
```

-	Layers:
	-	`sha256:4fa0ad1179db708d87405eb8df28d6925ea9f3543a7c91642fc75ea189aebdce`  
		Last Modified: Tue, 04 Nov 2025 10:38:11 GMT  
		Size: 7.5 MB (7487040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21a9a1e77b0197035bb229837a5b6d8a62d1eacc1b6268f9713086dce1d6b93f`  
		Last Modified: Tue, 04 Nov 2025 10:38:12 GMT  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e03000e68bbe2f75022f203250f2f55bbd6e06c2f10957321c1e7dea5364e1e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277474945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640e4001ae9c328a43446175c607db7ff67f3045fa2823350c8940395692156a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:44:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 01:44:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 01:44:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:44:10 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 01:44:10 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 01:44:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 01:44:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 01:44:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31125488da31bac27e6d40288dfb3b04b4e4cac11858e2cc74a28f6bdbc5d50d`  
		Last Modified: Tue, 04 Nov 2025 01:44:53 GMT  
		Size: 142.5 MB (142460569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc81589ea4886708c816c61a5649c87d5b697e4fccab4007ec4ad05e0d533eb`  
		Last Modified: Tue, 04 Nov 2025 01:45:13 GMT  
		Size: 85.4 MB (85363302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c2d17d87dbc2591fca245911afecce7ddb99e365961ec0189bc0f031980497`  
		Last Modified: Tue, 04 Nov 2025 01:44:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c59dbd23365a2494f3e1a86e6cf14097da3ada6a11154170c97f92ce34ff4cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7508991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccaffa7df04ba03a2efaa166b6ba691ae72808ac3a21183313574a700e898041`

```dockerfile
```

-	Layers:
	-	`sha256:605cf51ec2209b82a6c003bb3264794e4e2f1eb811cf1e91cb3d401a96c3eda5`  
		Last Modified: Tue, 04 Nov 2025 10:38:18 GMT  
		Size: 7.5 MB (7494688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25d63bfb606c5e1b9c96a02026cfcce9e5f10993a73c32eccbf771977141dcbc`  
		Last Modified: Tue, 04 Nov 2025 10:38:18 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:4a68fe5807636c13f7d22a59acdbe9f3ee788baf4b446514051561633a221f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.9 MB (276914039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb0a9d48fefc4ba632bedb22c27bfee155778e0c1ab3d5e7da62cf7af9e1bdb9`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 13:13:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 13:13:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 13:13:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 13:13:22 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 13:13:22 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 13:19:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 13:19:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 13:19:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9914c6aceb11166c2d07487ce797ce9fb3115772f158aab9014715759c9e05d`  
		Last Modified: Tue, 04 Nov 2025 13:14:50 GMT  
		Size: 132.9 MB (132853175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961252b24c951949dfb573f761a3ab43a86cdad9a1c9dcef79b1e9311cd793fc`  
		Last Modified: Tue, 04 Nov 2025 13:20:17 GMT  
		Size: 91.0 MB (90950091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849489f2f510b8c05a3f4ccc80fdc632bceda650ee3dd3db36a92589ef297d59`  
		Last Modified: Tue, 04 Nov 2025 13:20:09 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fe3d857eeb187c35220401bed160378fa23c4f47f04b314d0e8e17e8f58f07ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7504276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7921106e09857f58b43ba786a97c1bb80a2497e8f796b22b19ae624bbbf70e33`

```dockerfile
```

-	Layers:
	-	`sha256:d3ef592410015d0eb98b0996567aef29e96fb2415b91648f2f103ab9407e41b4`  
		Last Modified: Tue, 04 Nov 2025 16:36:02 GMT  
		Size: 7.5 MB (7490844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43b87416e223afa6ae9dbde45189b2bd91d24b34ac1d405f8eff639d25b41c19`  
		Last Modified: Tue, 04 Nov 2025 16:36:03 GMT  
		Size: 13.4 KB (13432 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:ed40eb9662490f3564b9980d25aa640526599e37e5d309c37f785d33a9245be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261483944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ba777f120c4115d8f84b1d80b9c563faf7de1da258bea23b7dcf3c56eaf9ec`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 12:55:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 12:55:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 12:55:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 12:55:15 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 12:55:15 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 12:57:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 12:57:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 12:57:35 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:48bd359f940d437208e8579c571291503fa327e04a66a6c8d918cfe93cae2e1e`  
		Last Modified: Tue, 04 Nov 2025 00:19:45 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc69aeb6f642e24b91c8abc7db1d688b36af067eb53670762bc030a8b22aca20`  
		Last Modified: Tue, 04 Nov 2025 12:56:17 GMT  
		Size: 125.6 MB (125622121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b63763566d304e47eed8c06d65d627d66a15a5ce8298080c688607db33eaa5`  
		Last Modified: Tue, 04 Nov 2025 12:58:16 GMT  
		Size: 86.5 MB (86508878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b805e4c45b002a1dcfe7ab2002a6433884f9083403848eec5986bbf0b1a05ef2`  
		Last Modified: Tue, 04 Nov 2025 12:58:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5c0615b10bc20e94bb863189a08cdc7e847e78bdf0d13a85e5dca21155713bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7496350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d54f1f6e8824d506a6d0015536ef1203bc7b2089ad2c1eda0a7eac15ed1eb9b3`

```dockerfile
```

-	Layers:
	-	`sha256:db7453fa8fee3092061162f5d667233327d038c130581f019a6ee73855814e82`  
		Last Modified: Tue, 04 Nov 2025 13:35:36 GMT  
		Size: 7.5 MB (7482966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55cb482ad8e8564672d3df02043e85c66f9f23c5a7b1856756cb7466f154b859`  
		Last Modified: Tue, 04 Nov 2025 13:35:37 GMT  
		Size: 13.4 KB (13384 bytes)  
		MIME: application/vnd.in-toto+json
