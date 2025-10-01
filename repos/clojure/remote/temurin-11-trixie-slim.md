## `clojure:temurin-11-trixie-slim`

```console
$ docker pull clojure@sha256:bb00eb5d44203b8475d0f2323ea4e6a3428bbabe953b57ac9e518c37bf9b9e14
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

### `clojure:temurin-11-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d0a57e7076de19201061d64c97c56c0390b574630a5ce752e8c43bded278dd65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247431922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e9114884b6993338a18ab2b50249115f3c72a9e87213462e59258b7f982d77`
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
	-	`sha256:97960a1513520f2eb61e5c85c785e659cbf2f3117c3572f6ac652f36181b6f0f`  
		Last Modified: Tue, 30 Sep 2025 00:52:10 GMT  
		Size: 145.7 MB (145658278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b633bd444d6ef7164e191971aa932e0517cba2bbb7b650b26e0685d19753a6d`  
		Last Modified: Tue, 30 Sep 2025 00:53:18 GMT  
		Size: 72.0 MB (71995235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86f3a1697395203eadb69baddae16245b131f5a4c0f4cc924d2d10e986d877d`  
		Last Modified: Tue, 30 Sep 2025 00:53:13 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:53b1d4225000b2f5c63b76c208be90bcf1dfc046898630a17f63a1dfefbcc26f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5290540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778d437592fdcafc423c1a36772405e4a1428ec8504573bf36553a9120241f0e`

```dockerfile
```

-	Layers:
	-	`sha256:7c35c185f4f79e27f04f417374a61b110ad457fe1c43528bb3e8e619edd01177`  
		Last Modified: Wed, 01 Oct 2025 15:37:14 GMT  
		Size: 5.3 MB (5276254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7d01d9716740052c7c1338ad9e85d21b684d0f5a33ef375fd54e4ebd18b5dc6`  
		Last Modified: Wed, 01 Oct 2025 15:37:15 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9ffbb61b9edef3aa3b533a95ba08a88a33106f6953f042afa35b854cb906246e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.4 MB (244404411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596fc2af36f4671460f1afbdb124255ba5571c44aaf7f8e13f6349b3684162fe`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e768f5bc5962050dc7cd7e82c8232f517b2f49b575cc96de5fcd6372840c3aa`  
		Last Modified: Sat, 27 Sep 2025 02:55:29 GMT  
		Size: 142.5 MB (142458757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a59d70bf72f1d2eff877d8793b876d8d19cafccbe655d08761db0f507273dc9`  
		Last Modified: Fri, 26 Sep 2025 17:54:49 GMT  
		Size: 71.8 MB (71808376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518ed59f9ca0a6eee9d045c57549a5f0f54002175fa8753ab3f3a24863c504fa`  
		Last Modified: Fri, 26 Sep 2025 17:54:28 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9b534c622977ba4367d2349d503af45353bff02f7ac1fb745a11c4025c5b2ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e602b877dfa83d48cb2066ca6aa97906eebfbea7c1cb7490e41471f1338153`

```dockerfile
```

-	Layers:
	-	`sha256:e2b5cd66bc9e228c4d77dfbd973428eed866ad56afd69463542d73881bb3cfb2`  
		Last Modified: Fri, 26 Sep 2025 18:37:48 GMT  
		Size: 5.3 MB (5282641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42da2ca321710bc4b8ba1db64cb2d176ca3a592a816bdb084b76d4ca18c1d4ea`  
		Last Modified: Fri, 26 Sep 2025 18:37:49 GMT  
		Size: 14.4 KB (14403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:881530c6e2e0aced2f4317eb1d19f7431c7dfa7552359394f40c5e79cec097bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243842500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf88555015bf967c9e9e5aba93d1c28dc429c43f89607f40fe638dedfe4fcfc`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd24a6000d0db05f3f61ca99b8bc75ccdd9e7e0398a4a8341532dc9e4de8562`  
		Last Modified: Sat, 27 Sep 2025 20:04:41 GMT  
		Size: 132.9 MB (132852806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8976f10d229e0b651f73661b528c9f6871ff08e60f10d0c1cee80eec07331108`  
		Last Modified: Fri, 26 Sep 2025 18:12:11 GMT  
		Size: 77.4 MB (77394698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd605aeb433f4b0c5e5a08dcf69844efa6fe832d6fd357c23fb84c3e36fd578`  
		Last Modified: Fri, 26 Sep 2025 18:12:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ae3e35359c163f17cbfe90be2cff00c7fe62b4aefa9829d98cdd1025ce1bf466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76dd277b145763d1985797f917c4f05784ce7831f4368fc506d7b21615b50b4e`

```dockerfile
```

-	Layers:
	-	`sha256:ef0905254ee1182bd0e829db764996e0c6ff4300f4837ff7d63f3ba0b08d0788`  
		Last Modified: Fri, 26 Sep 2025 21:36:36 GMT  
		Size: 5.3 MB (5280010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:113b91f19498a4afece6622177cb6b90fd41297d19c47657c858c5aec6854cfe`  
		Last Modified: Fri, 26 Sep 2025 21:36:37 GMT  
		Size: 14.3 KB (14334 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:3d762c2adf0ed817fa3385dc8e7d90ff9bdd0e184664e06de1c31c85c803d3e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228409575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f1aac4f77e5c821a74fa3da7699947e20e0e332e08d093d170f1b165199713`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
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
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75f5e71f328a32bd3c21f6959d2f275a0ac453b096e2b0d11b59fa89df37c1c`  
		Last Modified: Sat, 27 Sep 2025 20:12:57 GMT  
		Size: 125.6 MB (125622240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5890c85a9542fa9084b50af475839ee7ccc6c5da1ef9653e664444a921afeba9`  
		Last Modified: Fri, 26 Sep 2025 18:58:33 GMT  
		Size: 73.0 MB (72953784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84cda37a2b11d3a840aa8cd22cd7b301ac6bfd54336003b988d86ed0db1278e8`  
		Last Modified: Fri, 26 Sep 2025 18:58:28 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:40571b32f45e29ca9e63c6c7b9a0f96926481c2eb22fc196266a0944969fdd2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5286467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ff63c1049520963eee2ddf7d972adeafe6f7679b4cec5760d7ce36e3b0bf5e`

```dockerfile
```

-	Layers:
	-	`sha256:f046d62bd5ddc2b96d0132e5f7188cbc613ca50cb0df4b01010366d105a76ae6`  
		Last Modified: Fri, 26 Sep 2025 21:36:42 GMT  
		Size: 5.3 MB (5272182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aebb268046f39e07bb6896e63b4378e1aab10e67e9877fbf340e79e5513d6f3f`  
		Last Modified: Fri, 26 Sep 2025 21:36:43 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json
