## `clojure:temurin-8-trixie-slim`

```console
$ docker pull clojure@sha256:0f494c6b46d7d7fa061597d62057f9088321c1e0f096ebc9c22a3a5794804ee1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:daea9bdc1c93b0e1992496b2ca1221bb93f1a40d1d155643b3c4e80a77c26f46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.4 MB (159448106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d26b05b09d0dcfcc5e1fbbb160a33a96193978e7985d3a78d9eeb955935da6d`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f7f919518ddbe13979a63d296f9cc36ade96bf3fc043fccf3a02e61a346106`  
		Last Modified: Fri, 10 Oct 2025 11:28:57 GMT  
		Size: 54.7 MB (54731322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f942c05eaf7b6f0c866a7e5e0cbc29d4afbd2e5f656932fe82e5cf4cc89716`  
		Last Modified: Thu, 09 Oct 2025 22:26:37 GMT  
		Size: 74.9 MB (74938372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a582881c1f2b6a596c4cbec75fa74a988d4a53af8cf0886354984e4ccb21bdf`  
		Last Modified: Thu, 09 Oct 2025 22:26:31 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ef717a0d00af0320d2ca82f9cb1287209e00d8cb3f2a566f897ec18980e56dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5392048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b38530d031fd651ecf858bc0423846db76acad7180b19c3570d093907249759d`

```dockerfile
```

-	Layers:
	-	`sha256:44041c6335378fe873fc9ab939cb048cc3c03220fe7832fe3a994b7c6542f240`  
		Last Modified: Fri, 10 Oct 2025 06:52:57 GMT  
		Size: 5.4 MB (5377777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:320c84bcff7f8aab1d8eed9db64c8798f24c920bc175103e26bee80809ebed9c`  
		Last Modified: Fri, 10 Oct 2025 06:52:57 GMT  
		Size: 14.3 KB (14271 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c4b626910da14c687258e63cea7a272639a55884876010c7a3570ed729906dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159101809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf5475eb5bbb37a2157748af56abba80325d24c31bdd2ccab6b0978bb36c8cc`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f402f45755a9e3f0dc7448df1b886b547fe188f0402ce419b1c1e55ad485b82`  
		Last Modified: Thu, 09 Oct 2025 22:26:39 GMT  
		Size: 53.8 MB (53835624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d9521a27a2f3bd03422d5d837710a375b82839d3d5059f58b4e7b83fbd4465`  
		Last Modified: Thu, 09 Oct 2025 22:26:41 GMT  
		Size: 75.1 MB (75124699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b491b5fed24794dc679cb9f0b58d7aaa3d92f83685b0419196767df601ecc97`  
		Last Modified: Thu, 09 Oct 2025 22:26:34 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e70721a22ece18d0b2c9e9268d5e8105b15e89508a29227fd1b2c5070bb5db73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d856626d9050182015381e60cb4f3d642322e60bc3d43a833c07b0519ed81ecd`

```dockerfile
```

-	Layers:
	-	`sha256:6d82b1c4d621cf97c7b07e9f981dd7b131e1c3642ddd2355fd65cff994183fbe`  
		Last Modified: Fri, 10 Oct 2025 06:53:03 GMT  
		Size: 5.4 MB (5384244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a154bb9c6678b24823b3fd13b12f6777f1e80dd375fc3550cb9bf074c81021aa`  
		Last Modified: Fri, 10 Oct 2025 06:53:03 GMT  
		Size: 14.4 KB (14389 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:dd3a87d7d487c5e3b9ca97a330f354fc9d18b5ea3829c493a1faae5c751d14d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166352772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f24df693d9924351410c23fa04a02a19013e2263bf42067d9925430a5b95b77`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8850f6bfd7c5a8dd3875f0dbd8746815ac97b4f412c114102fd1d99799526a2c`  
		Last Modified: Fri, 10 Oct 2025 04:47:10 GMT  
		Size: 52.2 MB (52165392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0950612e1044930e7226f77d156aa1393b290600cd86d9f9aca2131b70b7b1`  
		Last Modified: Fri, 10 Oct 2025 04:56:17 GMT  
		Size: 80.6 MB (80588281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2b2c0fb131309dcb24978b0d381d0ddd0cb338198996a52811f651e0d8090e`  
		Last Modified: Fri, 10 Oct 2025 04:56:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8b970338235720b1a6a8db4a6288670b25fd1645f6a3850d2cffb829fbebf620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6875e71136e24efa7e82101bbcc7957fc9d00af953f968f8838418c27e5e1c`

```dockerfile
```

-	Layers:
	-	`sha256:5dc1bfabea2d19ca1c2a309fed9b845dd0e295e46a2c539df79bb59343a6192e`  
		Last Modified: Fri, 10 Oct 2025 06:53:08 GMT  
		Size: 5.4 MB (5382741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b11973620c6267bba6216dc24a86e42a2337beecbd0d51d65b66967f46a4a14`  
		Last Modified: Fri, 10 Oct 2025 06:53:09 GMT  
		Size: 14.3 KB (14319 bytes)  
		MIME: application/vnd.in-toto+json
