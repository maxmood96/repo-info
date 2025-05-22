## `clojure:temurin-11-tools-deps-1.12.0.1530-trixie-slim`

```console
$ docker pull clojure@sha256:81e9d7f7c4e201015053d70e4f65aaa240a3c17a9978f67ebc733171ba1d7997
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

### `clojure:temurin-11-tools-deps-1.12.0.1530-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:10c3f82fb2d6b6afc86c4c045d3319f7da124a9f55c5b85096cbdfea69ff435a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247114739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ab8e33666ab09acc723fdcff97d6fd34030eed4a0de50e0bcb5f491d05917d`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ced038dea045df288fe9bdbe03117ca66fe2a071217e196ac86ed07f965fe688`  
		Last Modified: Wed, 21 May 2025 22:27:59 GMT  
		Size: 29.8 MB (29755384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2d1c7d2f9c50fb49dd5ce27765aa373c678754d1463fa4cfdf9e21373ee77d`  
		Last Modified: Wed, 21 May 2025 23:32:37 GMT  
		Size: 145.6 MB (145635719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbdd87d2fa6407bca6ccad4f8181ed70c48587e83a6555c6b42fc1cb7c9df0c`  
		Last Modified: Wed, 21 May 2025 23:32:36 GMT  
		Size: 71.7 MB (71722993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37009d7ef20542489399fa2534a08ddd36a3716cdb49cd7c9b04a4546f87eb69`  
		Last Modified: Wed, 21 May 2025 23:32:35 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8a338cd7a0690f1e7f6f4753575c68c837b0030073d1f458ab8f7c3ec62b1806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5146492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8570216df813271249d3116cbaadbc18cd79edebe5ea6aaf7ffed40d4b9fab06`

```dockerfile
```

-	Layers:
	-	`sha256:80d2cd929da857272d41769ca9ff90e5ded96860342f7be4ea28a05b50755b6d`  
		Last Modified: Wed, 21 May 2025 23:32:35 GMT  
		Size: 5.1 MB (5132206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f7b934d29032431f6e0e872c450037e95f37ac43d048b2df465b3e0379de888`  
		Last Modified: Wed, 21 May 2025 23:32:35 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1530-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:30ebd3b64ef75377dda12858b8cd10a82ad071f8d2c62e502eecfd3f5c7779cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244187315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7845318144d2b7eedfc61971cad6e1affd64ccfb701e7f20244879d4c9d8d61d`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6098c2c9fa277c00ab580ce12bf64a9e1edf9e9139ba18ad85f3cc3063834aa6`  
		Last Modified: Wed, 21 May 2025 22:31:23 GMT  
		Size: 30.1 MB (30119455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600e5890186e5b38237e942490eb983789f9f316084b6dcb817110755050b5f9`  
		Last Modified: Thu, 22 May 2025 08:13:51 GMT  
		Size: 142.4 MB (142420736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385479908fb202c9b7b30fea021b1782efe7133ff98d07f90313f8d833526dfc`  
		Last Modified: Thu, 22 May 2025 08:18:05 GMT  
		Size: 71.6 MB (71646479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ba291610c5a6986f58a9e4eab45f0f5da84c684ad18db74ea7b4b905096991`  
		Last Modified: Thu, 22 May 2025 08:18:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b7ff8bc4889d6bbf3296ae3decd6139abc79e885c5fde95f6a0123dc5ee186ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ccdcae14a9e4101eae8871c6faea8b5c7616151dcb2df6f7a4fcd5d74c1a470`

```dockerfile
```

-	Layers:
	-	`sha256:0043f8cf99871365f79fc64feffa5d52c82aaefd32b82369381536e84844e345`  
		Last Modified: Thu, 22 May 2025 08:18:03 GMT  
		Size: 5.1 MB (5138593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8b38512eb22b6b76b84f9673598315dc56e91b30cd859ca78d0c76e31ac9b1d`  
		Last Modified: Thu, 22 May 2025 08:18:02 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1530-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:679c2cfdd6262faaa7634b6eff3453a1ef1a0774038d832337e6c82aabb53aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243607201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c04d854e9d0e920e352cb83aaa41fdcd1b8b44fdd617372dd58d84a0f9b4356`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:62eecea9deba6eaccef3e829ddec51f2c540dbbb668a68816c8ce3c4b8023d93`  
		Last Modified: Wed, 21 May 2025 22:32:27 GMT  
		Size: 33.6 MB (33580565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562563506da04808bc8de5e7cfb3093082bd8e844ad4b319d9831f07229a0244`  
		Last Modified: Thu, 22 May 2025 11:05:17 GMT  
		Size: 132.8 MB (132809834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f665470fee4595b8edba913a874b66606dcfa38246906eb89e06968b6703e646`  
		Last Modified: Thu, 22 May 2025 11:12:26 GMT  
		Size: 77.2 MB (77216159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd16005a23975a8e7f9d1a431d6878da7860b9218b35037a86ee711e622cf54`  
		Last Modified: Thu, 22 May 2025 11:12:23 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1904bc4911772e2530bad9e789e8791ffaff6f061a2dc2c98551a386f816e824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55daf76bbeb9272f319a2f5e75663d4db5fb901645f5b743edb2c95e0d975f05`

```dockerfile
```

-	Layers:
	-	`sha256:724836667880f28ee6832f5431cdb87edf5862b69b10d61dca9f76faa42ce8ae`  
		Last Modified: Thu, 22 May 2025 11:12:24 GMT  
		Size: 5.1 MB (5135962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eb019225d74f852397af94a7f3143ddeaa2d62e32181a08f6f180e8480026a9`  
		Last Modified: Thu, 22 May 2025 11:12:23 GMT  
		Size: 14.3 KB (14333 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1530-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:17d316ae9e0d919f03943c08801a0d800d183fdb62300e20a753b6946ab7055d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228228309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396508f4a6504eee70aacdfdd7795d40fce59a0133fd5a029020bc060ec51639`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7cbda353d6047374e3da60bdf79ae89f8047840010f0964c87a8f2714e146106`  
		Last Modified: Wed, 21 May 2025 22:32:10 GMT  
		Size: 29.8 MB (29829620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f378c47b9b0bfaecee00f49006cd7201176fb0435199f16f9664d8506f3c1230`  
		Last Modified: Thu, 22 May 2025 03:41:47 GMT  
		Size: 125.6 MB (125585838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb10f318369eb844a0a88d054eedae4d05d11d83d923d2dec2d02311880b540`  
		Last Modified: Thu, 22 May 2025 03:48:27 GMT  
		Size: 72.8 MB (72812207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982453079e92197ad7033e20b0ce8530827c9dee496d786b9bf9a8a94ec24781`  
		Last Modified: Thu, 22 May 2025 03:48:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9b4e268228eeca2cef0e30cf128f1bf16de199bac40012be7e412646b9fa379f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5142420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5e3499ba7bf91137cd2c52fcbe0e34e088f598cdadf8f8d9c9fbce168b3b79`

```dockerfile
```

-	Layers:
	-	`sha256:04d2a05e08e4d74d2ebd206625b3d53afe49b352d04bb0215aec0ec291c2c9d6`  
		Last Modified: Thu, 22 May 2025 03:48:26 GMT  
		Size: 5.1 MB (5128134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec6bf96cb254a3ec44d31e69591ae492561e2523364f7b2e9ddb13cb82780add`  
		Last Modified: Thu, 22 May 2025 03:48:26 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json
