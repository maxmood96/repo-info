## `clojure:temurin-11-trixie`

```console
$ docker pull clojure@sha256:5c2c8af8fa525484d66e02b732264abe900fd527bd038d28fb4cbd782184b5fe
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

### `clojure:temurin-11-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:e6550d3d21f31108aba3ee7bec6513afeb2cc0033ddf36353c904b126f7c8a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.1 MB (283090377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584b4eb646599db1f7801b87093a98c5fb35197a1aff6b8cc881bd59bc9d4ad5`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28420c33f9ab500c969026ff796e8be979d6780a674398d043716c00e1ed424c`  
		Last Modified: Thu, 05 Jun 2025 02:46:10 GMT  
		Size: 145.6 MB (145635638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a846d15c539c3815014a2154aecd3f9eaf65c19a589bf405251488088e16115d`  
		Last Modified: Tue, 03 Jun 2025 18:24:36 GMT  
		Size: 88.2 MB (88207187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfa18bd0d0acbe5baf93d3e9c04406733cba86d30d080b5ab93cee16371c7b7`  
		Last Modified: Tue, 03 Jun 2025 18:24:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f508fcf8c512e4365552c88102e6d886c803408f59179640451f1cca2964f1a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7352785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35651b9b58653a1ddb5cb09a439e862e30d031a98e02c43d93e4455d81cc5a25`

```dockerfile
```

-	Layers:
	-	`sha256:ab412bae4ffbb825b6dcdf8a711a04ba0c916d1a1f7327c60ced3c2a03a51d05`  
		Last Modified: Tue, 03 Jun 2025 21:36:28 GMT  
		Size: 7.3 MB (7338557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d6fee49c50c7763462b069f765499f092fdfb833cd39fe8280915c1f321c074`  
		Last Modified: Tue, 03 Jun 2025 21:36:28 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1d96593fd44a88ff0b3c4d2fec0e67318dcd257be7176da815ae701c96198968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280550756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4db5dab1eeb849a1e1446858e36176423b183a7f15474daa5595ca6c392ed6a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Tue, 03 Jun 2025 13:47:15 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6427a95fab6810b7c6cdb6297a4f0e9dd4a6bc046279a099df2fde01100b9e9b`  
		Last Modified: Tue, 03 Jun 2025 10:44:50 GMT  
		Size: 142.4 MB (142420666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a30da3d5442d31385f933e9441928117f0ac5515b50ce67560c8040147c0f93`  
		Last Modified: Tue, 03 Jun 2025 18:37:42 GMT  
		Size: 88.5 MB (88511154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98c870c3944690bfa91eca677edbec2848be3e81f7f44d1bbeca32ad1f27c6a`  
		Last Modified: Tue, 03 Jun 2025 18:37:19 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d667ad7f0dff24771f077c79fd8363c706ed5cca3d3e536f5f6e93e1b01c6af5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7360551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041dbce1b03f8bb90740fb9d3f69484b8d4c1ff4817cbe659068e75392c3ac5b`

```dockerfile
```

-	Layers:
	-	`sha256:84dc4a16e7ce81d4a5d7938469313b91eaa990e4fb8af232071826c726b07783`  
		Last Modified: Tue, 03 Jun 2025 21:36:35 GMT  
		Size: 7.3 MB (7346205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60c669a9532a8569363a2f9872717473b5adf4554c9bdcbe6f0dd623fba92208`  
		Last Modified: Tue, 03 Jun 2025 21:36:36 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:2c57d8e694d51bf3f05bab377c61e42dfd6d9ebdd08986cb486650e048ff27be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279841877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24726462991a4c5e63802611dc3475a4783d1472bc344d65b37d7eb893728855`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:25dfffa4126a91eb76c700c90bfdc9a9e15f34c7438a81f16c8a6999bbde6e45`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 53.1 MB (53080544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39291d7ae4a9e82fc2c95d75539cc21cd0bc9715c3ac4d5b032793f128324bb4`  
		Last Modified: Tue, 03 Jun 2025 08:31:55 GMT  
		Size: 132.8 MB (132810533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c3003386bbcbeb806f3002f8d175c9f2c6878ac1883c1eb723620a0701f85c`  
		Last Modified: Tue, 03 Jun 2025 18:45:51 GMT  
		Size: 94.0 MB (93950158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8b8f15a8950467ae4013697e2c36dcbc10645031892ebc5fa021b89e2b3ddf`  
		Last Modified: Tue, 03 Jun 2025 18:45:42 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:cd2ec577d84a33b52ec0fcf9288ade7c560752da6dc3edd3b2fdf01a596b475f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7356635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9c68e8ce42e0b0fa52c95e9f4207efeb878074a53b07c1020097b759756884`

```dockerfile
```

-	Layers:
	-	`sha256:f48f2683c5f321908e1c573553fee0c32bfbf327f1ffb9f841768ee8cae47869`  
		Last Modified: Tue, 03 Jun 2025 21:36:42 GMT  
		Size: 7.3 MB (7342359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b66352691197299a97f957a04a7aa031ce10a2f72151c7019fe96cbc804f8d53`  
		Last Modified: Tue, 03 Jun 2025 21:36:43 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:880e0a603445e524bbc5d49d821b5753e3e53802f49bdd6f35bdf3d6a02b12d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263861407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb7cc0dfe7237af6ec4d8d314ae37d87fc2f73507068f78921b3cc990a3028a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:71c8524b25c34592c256fbae9045d0ade48f5e9889d37c5b2190092fa9017d48`  
		Last Modified: Tue, 03 Jun 2025 15:34:07 GMT  
		Size: 49.3 MB (49322227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3809b7d5c48c969004e20fea95a6f198fb053f68fc077ceacfe71f6d2bf50ddd`  
		Last Modified: Tue, 03 Jun 2025 06:04:23 GMT  
		Size: 125.6 MB (125585319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b654c5895acefae3fcc829b32845c3e5d3d20ec87168faf768707ffda033d9`  
		Last Modified: Tue, 03 Jun 2025 18:29:30 GMT  
		Size: 89.0 MB (88953216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97559f845c7295994e4dc79fbf5d4480c8700485f329a29ade1c4b8c5f5d7c2c`  
		Last Modified: Tue, 03 Jun 2025 18:29:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8788614495a659869c40a448f5312b157169375ad36810170eac8a5ace7e9532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7348711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e999d43b21be914507509b978b2351e84532a8a42d7f7b92f0993510712d9ef`

```dockerfile
```

-	Layers:
	-	`sha256:b448bb061b3324d7358ed8488db05e8718cb785dc5f94eb24f9842eab14fc936`  
		Last Modified: Tue, 03 Jun 2025 21:36:49 GMT  
		Size: 7.3 MB (7334483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73aca426701bf97a2f054c5a36a104e053f252ad9c84031d80d0c931619e8091`  
		Last Modified: Tue, 03 Jun 2025 21:36:50 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json
