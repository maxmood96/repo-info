## `clojure:temurin-11-trixie-slim`

```console
$ docker pull clojure@sha256:b25aeea62d9746080f8d21a6999e49b72988d3bc2422299727c69ce8577a9f87
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
$ docker pull clojure@sha256:76ee63f50ba1d8b92dd9c45d3889d48d102120d99525ec1182aa640a0ac325d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250066122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16b159b92087c4b6bc2f0c200ffc2bf61dbf7c67f41a780705228e6434df3d0`
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
	-	`sha256:835abffaecb017dcd56637ac2642b0ae4100167795d75237e0452c5c4b63a306`  
		Last Modified: Tue, 03 Jun 2025 05:16:15 GMT  
		Size: 145.6 MB (145635604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44003dadda2a40e41eed80dd6e39fd7396505f8c483d8471939369f142a988cc`  
		Last Modified: Tue, 03 Jun 2025 05:16:13 GMT  
		Size: 74.7 MB (74674491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6c841f670c84edcc5e3c6d3005b5df39940ede9643ec2224401f70ef24961c`  
		Last Modified: Tue, 03 Jun 2025 05:16:11 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:94642beac7e538584932bd8750f4747ff3a8c576449b556733dd1daf48b71893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5146492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5de176c1b32ab29991722349532243626df7558265b819d81ae2ee1040bc232`

```dockerfile
```

-	Layers:
	-	`sha256:d700ca4fe07f968d7be21266f6466908922155444e88d81f4dad16d1039c98ba`  
		Last Modified: Tue, 03 Jun 2025 05:16:11 GMT  
		Size: 5.1 MB (5132206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:080a486cad77ca9dd2878ac857f5bb78f899f85625e1edce1c1329e1f0dcc48e`  
		Last Modified: Tue, 03 Jun 2025 05:16:11 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; arm64 variant v8

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

### `clojure:temurin-11-trixie-slim` - unknown; unknown

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

### `clojure:temurin-11-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ab9fa59060ed4dac0ae36f4d8581ea987c6cfa0b878e6581bea9dda0d5fbcde9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.8 MB (246805846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ddd59f49371651f18c5c2edbe4f144392764594ea2b013984a0ef31af1c6ea2`
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
	-	`sha256:51c18682abc822fc2db69cf01e2aaa0cd74ec88d2153d1db29a25210375b8100`  
		Last Modified: Tue, 03 Jun 2025 08:33:50 GMT  
		Size: 132.8 MB (132810533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ca3cd7ecd71ba05cb421fc2f07af2effa14a5e38ba9329bd9cb0f3e5805c6b`  
		Last Modified: Tue, 03 Jun 2025 08:42:45 GMT  
		Size: 80.4 MB (80414104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03322fb8b0d7b91335de81e3a89625afd0431cc478216705cdfa0320645d8e27`  
		Last Modified: Tue, 03 Jun 2025 08:42:42 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:11d02c7502a31ea4e9503a59f63a2b7e33e9eb045574e9b2ae66a467b0b12ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db972efc0d3e83e5a4e8f73aaa135f266efbcd5ab729170ec6724d31d6936e20`

```dockerfile
```

-	Layers:
	-	`sha256:24ad8194b452c60c4543818b97ba905dc5c301e975b7fdcb2b3eec7ce875f61a`  
		Last Modified: Tue, 03 Jun 2025 08:42:43 GMT  
		Size: 5.1 MB (5135962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9b79a89f0719caf95d23fd3a07ee29a6423f7fab252a4d5cf1dfea640994507`  
		Last Modified: Tue, 03 Jun 2025 08:42:42 GMT  
		Size: 14.3 KB (14334 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:7ebe27646e1837577d3a36c7103a97ee9cb2595a30b3c103d7eda7613be0c349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230821594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a60d523ed1eb665a139d9d550581c87eb341b1bcc3e0ff630cb32bba3e13f5`
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
	-	`sha256:3a6e2d8c49d3bdaa5b7240371085b6676318ff2eba1026dddbb17010c7fad79f`  
		Last Modified: Tue, 03 Jun 2025 06:05:26 GMT  
		Size: 125.6 MB (125585353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3128ab5dd704c925e57d33f169cbcbad7fc074e58f59e660bd0ca24d41874d81`  
		Last Modified: Tue, 03 Jun 2025 06:11:20 GMT  
		Size: 75.4 MB (75405979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407c6b8555c47329451bb924a82828a1f36fb3b0686b7f4d6daa6933002de1e6`  
		Last Modified: Tue, 03 Jun 2025 06:11:18 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ef03c9a3d56a843d1bdb5e0343c1a838452858b83fbff922318b99abdf1e8341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5142420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e5d14bcfab31671d3c7657f68838d6ba1c10780aaee869b4b9f6ff90eef52b`

```dockerfile
```

-	Layers:
	-	`sha256:421af554ffeacc9f2d4f161e3914ce01af34c60f4f549839764fb2c0dfa9b39a`  
		Last Modified: Tue, 03 Jun 2025 06:11:19 GMT  
		Size: 5.1 MB (5128134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3ee3be92c0f2a830d781aaba6c5819260f361578dde1857b8eab58c5e4b03ec`  
		Last Modified: Tue, 03 Jun 2025 06:11:18 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json
