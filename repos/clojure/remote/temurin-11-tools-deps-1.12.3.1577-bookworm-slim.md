## `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim`

```console
$ docker pull clojure@sha256:3237f14a0f4432a2ea0212316a73eee6a4a102ea2a51dc9d2fd71af886c6326b
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

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c6a0d8b8b57e4e6bf48c9fc1c19e1ddf17625ff410fa5e38070cd9e0604b365f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242875149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:798c58c97bfb0740d5ccc1e11a07a539348244e7ef2f0ca429d354006c494fda`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:51:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:51:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:51:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:51:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:51:20 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:51:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:51:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:51:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f61acf7857a01360e0dcac8799f28a5c67b42fdce3cddd1f6b8f5cc8d566920`  
		Last Modified: Fri, 14 Nov 2025 00:51:54 GMT  
		Size: 145.0 MB (144966578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b06d76915cfe26814d5e356f2ea1e808bd8a9a91fb06db05d18f228858615d5`  
		Last Modified: Fri, 14 Nov 2025 00:52:07 GMT  
		Size: 69.7 MB (69679358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c905d8960c099413d983f99f78fd76afacda6018f503436bea5b040942eb996`  
		Last Modified: Fri, 14 Nov 2025 00:52:00 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7684da87617df26f023ae4a7be0cd51be9f86a763cbafdbd5fd69913380fac70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5147796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69669ea0d2deef0ab5acc34ecf2b48595e745f802fcf502eff17c64ff316ace`

```dockerfile
```

-	Layers:
	-	`sha256:c0488166630593e280165cadc4ae84aac5c1d1d5bee43ea08099cb8263a9ec39`  
		Last Modified: Fri, 14 Nov 2025 01:35:34 GMT  
		Size: 5.1 MB (5133529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abd72a571016d81ebc7abcc41fa9bc5f836f18a5c4e9e58974cf05ce2832eb9f`  
		Last Modified: Fri, 14 Nov 2025 01:35:35 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9646dff0e3ce1b3580c72675dadc9f9b221a03140a62fc0d419569b4e7d66e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239394941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcbde875cdec0c97a764e8162df340acf640d75c8e81dacbfed0bd238cb1c4f7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:53:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:53:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:53:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:53:11 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:53:11 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:53:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:53:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:53:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d08ca77c06e31e7c6f1ff9c1f0ae4034c4021ffda1b41c473be82bb76c928c6`  
		Last Modified: Fri, 14 Nov 2025 00:53:48 GMT  
		Size: 141.7 MB (141731549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10571f271422ccfbd7d22489338220bf196acaf2311ab33efd09160033db2ed7`  
		Last Modified: Fri, 14 Nov 2025 00:53:59 GMT  
		Size: 69.6 MB (69560369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7eee3d254d2d1c829d01cb26221826d1bb62b6c6e65a91b6a7057152b5c4b2`  
		Last Modified: Fri, 14 Nov 2025 00:53:54 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bec2eb5a31f6e2bc78ca13088b2d89742952c83baa03075a6894a84effe43b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5154293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fe5a13e12987d0a5e8ed37d673aa248d57bc3734c71bada4ee5b7fa522517d`

```dockerfile
```

-	Layers:
	-	`sha256:26fc60a7e43640bdcb814bfadebfa3884997f655b6f911fc042e6135cc784914`  
		Last Modified: Fri, 14 Nov 2025 01:35:40 GMT  
		Size: 5.1 MB (5139908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5a5fceed31d94739db2cbb123e253f1c330815af085334867d7775fa2c00155`  
		Last Modified: Fri, 14 Nov 2025 01:35:41 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2c862fad9086c5da5f3d4017774e20587cd4d1d51f21ef7504b5d1f3eff160c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.7 MB (239662629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fa07abd6fb73127730533bfb740a4dd9bd8c03635a0fc28510641ca8b78988`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 19:25:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:25:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:25:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:25:14 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 19:25:14 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:32:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 19:33:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 19:33:00 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec7cbe3d3d06402157351db4258906cf4ebdb1660eca1058f05eeb89ae2d1a3`  
		Last Modified: Sat, 08 Nov 2025 19:26:26 GMT  
		Size: 132.1 MB (132079869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d1e6b4d91e9cab920ead52c4cd809e0223e7bdd89b36d548fc2707e33dee84`  
		Last Modified: Sat, 08 Nov 2025 19:33:46 GMT  
		Size: 75.5 MB (75513210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b91340fcdcd7064ed67f53478cc621aa7be057fe89b291bdba30a23b39990`  
		Last Modified: Sat, 08 Nov 2025 19:33:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ddf61d68cffc8855e42b1e270c8912f3ccac2514e5c2b6e25fcbb9cfd63fd578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef2728a5ce96e3907323aa71441005fe3bea28b96dad66183bd427c1fdcdcff`

```dockerfile
```

-	Layers:
	-	`sha256:4d3930f10e3a67d03bb143e981bc6afd35454440a2cf5ac712144cd3caba2923`  
		Last Modified: Sat, 08 Nov 2025 22:36:45 GMT  
		Size: 5.1 MB (5138072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76ecfe0676ab0543297898ed8b45985e69e12825332d7b7899791dcb9233494f`  
		Last Modified: Sat, 08 Nov 2025 22:36:46 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:dcd9b1c903eba93d035e614e63bb44dd0743627507f8c9c53792bce1284864f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221070451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ed17c1adb4babb3ff52db7f6278d44ead0bdf7c702cfa722d1f220823f14a6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:50:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:50:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:50:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:50:52 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:50:52 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:53:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:53:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:53:30 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf795af4b4ebf64e8df25e33536bfb397427d27d924bdf9dc6c1f3d014458b5`  
		Last Modified: Fri, 14 Nov 2025 00:52:10 GMT  
		Size: 125.7 MB (125694442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307f68035eeb28ac39d027507ffd7661ef3c818ec555a8f0b22cbaa4647066e2`  
		Last Modified: Fri, 14 Nov 2025 00:54:05 GMT  
		Size: 68.5 MB (68490814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f110d78d91e30cb37dfd265f572bdc32f77daccb046a660e70cbd9ac8e38905`  
		Last Modified: Fri, 14 Nov 2025 00:53:59 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6de759381e59c8f18729031dd725a645a970598aa6945869ad0e037dd92a148f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4422098aba5869e5d3a19edd6181b9553cbd1eaa6c194116008c4ee283185d`

```dockerfile
```

-	Layers:
	-	`sha256:7816ed729bba1e8a7d867fc64cbe91ffe1ce64072362a93fd2079f3dc67a5fca`  
		Last Modified: Fri, 14 Nov 2025 01:35:51 GMT  
		Size: 5.1 MB (5124854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ed82701919729f51ea2055dd0bf75615ed5c9f137ca99f19cb58527f03754a2`  
		Last Modified: Fri, 14 Nov 2025 01:35:52 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json
