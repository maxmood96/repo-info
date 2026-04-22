## `clojure:temurin-11-tools-deps-1.12.4.1618-trixie`

```console
$ docker pull clojure@sha256:cfe599dff07847187f5f0a82296d6ef6ddfb26126444ee4fdd626b30f8e73ddc
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

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:354e92ab5f3051c8848120dbbe4e4c7b88cfd45ab3030f729e6a6cb191c0f404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280680020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e049ac10a563961eed08e2000197619d3e3077ecb314fa4f65c292ba636a110`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:17:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:17:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:17:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:17:45 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:17:45 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:18:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:18:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:18:01 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89eecdc4dbf72aa0946f6decc6658b6414a9a7b58bc79496810e74ca677be15`  
		Last Modified: Wed, 22 Apr 2026 02:18:24 GMT  
		Size: 145.8 MB (145806834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0465079c53e26ecf4db3f59be40eecbe3d0fddd1811348eff69e00fdb6be9d03`  
		Last Modified: Wed, 22 Apr 2026 02:18:23 GMT  
		Size: 85.6 MB (85570438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6814198bd328e46983fd08cfb702d5b454fdddbd7d18e2a88d5feecaa62fd64a`  
		Last Modified: Wed, 22 Apr 2026 02:18:19 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:71f3647ffdcddc46c39f8988ec253b8a6c16d4823b48b73bf08ec92553bb9d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7505046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70fced830980870885d7ef9cd0009d94e745473b52ca04e785856d501faae631`

```dockerfile
```

-	Layers:
	-	`sha256:6e080e094ebe4f52e9c76e80fc8da819945e5e7099a880f2de66a45f7b3b6f7b`  
		Last Modified: Wed, 22 Apr 2026 02:18:20 GMT  
		Size: 7.5 MB (7490862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e051f5b4269a76fdfd798a3c467d7100e2c70700c219d12a5596af484f91c25b`  
		Last Modified: Wed, 22 Apr 2026 02:18:19 GMT  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:86c58768350e3b52b6d47bc7ea1b4eab201a81c6dd18f1303efc5d3633a0ad66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.6 MB (277554301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062402ec79a0134d811c1dd2275c4130cf983dc0ae8dd8e6c302d9ca63bce8ba`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:21:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:21:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:21:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:05 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:21:05 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:21:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:21:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:21:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6a444f09dd737f5123041a14d335d772c7b07d520188f1f202e91f3ed8bc69`  
		Last Modified: Wed, 22 Apr 2026 02:21:47 GMT  
		Size: 142.5 MB (142500831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7eabcd0994ee435b54779eb4ad968a1242190df1e9baf688b773fd30c9182f`  
		Last Modified: Wed, 22 Apr 2026 02:21:46 GMT  
		Size: 85.4 MB (85383583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987b97db6f4c3287f65e8928ccf4e342180e3a6d95046990648ad6320283312d`  
		Last Modified: Wed, 22 Apr 2026 02:21:43 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d0f12dbc7ba7fbf719330a94b28bc56ff110ee3b1772ed11b9c42dd18571e099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7512813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04738322d6e42afa0750cf1af29be457bca612a21b4709d6b3b46eaa0a9bcd5e`

```dockerfile
```

-	Layers:
	-	`sha256:7d5d2ac18504ce371c4b81d4e7300f7579fb20771a68616820e506adf1e27eb6`  
		Last Modified: Wed, 22 Apr 2026 02:21:43 GMT  
		Size: 7.5 MB (7498510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2eeb329f9285f6695ba6ee9d66c6dbb23e0f27c5bad1d4d3713a0d94bd21dbd`  
		Last Modified: Wed, 22 Apr 2026 02:21:42 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:3d24ae3ec0c2086d2663bef8806c641d2b2f4180463c2627fcf6718113a56b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.1 MB (277107470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c0b39514be3966e74e04732fb4b150439cfb71919f6eea4dd2bb0f77ab90e7`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:22:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:22:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:22:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:22:31 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 08:22:35 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:27:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 08:27:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 08:27:43 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3730c515230ceba2109e879cebed0883fb00ea2c65355759d7c6c75f60fd28f2`  
		Last Modified: Wed, 22 Apr 2026 08:24:04 GMT  
		Size: 133.0 MB (132997390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482801a23af4453179b231faabf11d83eb249e49fa01853b27474b217c3213d5`  
		Last Modified: Wed, 22 Apr 2026 08:28:20 GMT  
		Size: 91.0 MB (90986453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f53b8243c646e0bcd1c5f6a7960855b4b7d201babdac7b844e1b7905cdec883`  
		Last Modified: Wed, 22 Apr 2026 08:28:18 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:96e14ff8e491763989f5a8fd6162b69f43222f5a16434718d99ebc50ca906bd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7508901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57e6498671bbabbaefa9fba1ed8ca23310b3bdf21f5763789962fa21ac39b8e`

```dockerfile
```

-	Layers:
	-	`sha256:be1d346183221c265b9e54b9a86fcc79b86db7ebf69a8887ffb6756eccbca3be`  
		Last Modified: Wed, 22 Apr 2026 08:28:18 GMT  
		Size: 7.5 MB (7494668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a626df185e36c0af2fd388cef045a1247cdaf3951ffd68c8f3c50b03e0d4e00e`  
		Last Modified: Wed, 22 Apr 2026 08:28:18 GMT  
		Size: 14.2 KB (14233 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:0715f3fc60220c1afcb0a81a2d1ae0d1aa1a3ada71300176462c8803b248a9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.5 MB (262478650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6605e0c5640db10cb199a30e028597c95830867027c10b34328ce638190eab3a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 03:58:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 03:58:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 03:58:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 03:58:26 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 03:58:26 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 03:59:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 03:59:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 03:59:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8e0b2edc82a3ba082e9f30dfa4358139881cfd62d2d6d055012699a091c83c`  
		Last Modified: Wed, 22 Apr 2026 03:59:03 GMT  
		Size: 126.6 MB (126562180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc291cfa33ce83706b87200d17371316860f9bcb0a61815e540ec921a0de9d81`  
		Last Modified: Wed, 22 Apr 2026 04:00:14 GMT  
		Size: 86.5 MB (86543720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc976f0a850c6416dde7325b963f58c26fe5d42e74c9ae2fc1789a5e5c2e022f`  
		Last Modified: Wed, 22 Apr 2026 04:00:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:72936774a58e86c184f08db28009f69cff8774597e5f937633364e49a47590d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7500973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f80cd2ce7481c0684f185cfe4e0d50b73d0fdf7c5211ab1349a6a3d8683023`

```dockerfile
```

-	Layers:
	-	`sha256:ddc9f65a0e6d15dad62203d0de4863ae9d43a4e1c65340a7c65dfe649c555f30`  
		Last Modified: Wed, 22 Apr 2026 04:00:11 GMT  
		Size: 7.5 MB (7486788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:065d94966ba4b9a83a9ab75c165a9a3c5f31ee7668cf6c97cc7a5cafcc97de4c`  
		Last Modified: Wed, 22 Apr 2026 04:00:11 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json
