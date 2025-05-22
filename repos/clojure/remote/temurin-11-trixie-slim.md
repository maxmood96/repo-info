## `clojure:temurin-11-trixie-slim`

```console
$ docker pull clojure@sha256:7ef426eab3455f340ffd3eae6c1a30b2f4c9d81cb404e612aeac975ffe8271af
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

### `clojure:temurin-11-trixie-slim` - unknown; unknown

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

### `clojure:temurin-11-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bfbb2665f4137528827357ded9eecc55d9cf5e424e6cb70486e221218dd4436b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244197534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27d4e2dc70da51495f784cf3f7ff80ac230bda9cfed1a3dd2fad9f47a63d58f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1745798400'
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
	-	`sha256:d0342bfffaba1a8be0950e44b5334c6cf9a05d9eedd81a042ec7813ac91850a4`  
		Last Modified: Mon, 28 Apr 2025 21:23:36 GMT  
		Size: 30.1 MB (30130233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394cb701603cc841d1cc1d1ad27378dbf17582cee266d468265a01aaae9a60ec`  
		Last Modified: Tue, 13 May 2025 17:58:05 GMT  
		Size: 142.4 MB (142420736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393cfc287c1fec5cb904c2221ec15940d11b9ea9f04aec2841bacd2a7e5b73fe`  
		Last Modified: Tue, 13 May 2025 17:59:37 GMT  
		Size: 71.6 MB (71645922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3c8ba0b83e12be14fa152d6899f0aaaf5a4c68accafffa97ce9326f8fa74e7`  
		Last Modified: Tue, 13 May 2025 17:59:34 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:103e8bba03e1614c8b06cbd3ccf3ea03d457164f6f7f79f36920bd7a5e67d8c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5107619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4a6d778373ec6a44ee65d208b313259518900e42b253e63ec735547141da238`

```dockerfile
```

-	Layers:
	-	`sha256:91b814dc4fa77865e12c16dd2dab3a61655473a0ddcfde973695a5c43aabe9b7`  
		Last Modified: Tue, 13 May 2025 17:59:35 GMT  
		Size: 5.1 MB (5093215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:181e1fc63cdd84e1b617db6026b8c5bebf8e24893f621ad31972e3913341e05a`  
		Last Modified: Tue, 13 May 2025 17:59:34 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:875079d23f1ffc92b26105dc7846a70aa37ec22a0c5f5e2a2c1148849740817b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243603111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0262f0782a2f7c896b0960b00b7cdf31c56c9db69cf2e026ec7ebb5dca694d2a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1745798400'
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
	-	`sha256:a739447e8599431e1e4996b4b6d4022822d37eddea9a3737acbea74b8a860d49`  
		Last Modified: Mon, 28 Apr 2025 21:25:59 GMT  
		Size: 33.6 MB (33577694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a20e2c1dae1640014ab6fa85e5ac56c9c5b5992d7ee7e9a915c99170e00b082`  
		Last Modified: Tue, 13 May 2025 18:36:27 GMT  
		Size: 132.8 MB (132809819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddd2a9991975868081fd8778e0a275e861cc167aa874b9546dd572d966eb710`  
		Last Modified: Tue, 13 May 2025 18:46:07 GMT  
		Size: 77.2 MB (77214953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b79bb657146c08440601faae799bd316eef44bf2d7af3110ac9d386d88d239`  
		Last Modified: Tue, 13 May 2025 18:46:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dc145cad3db0d9db8a57658c1b8fbfc4dcb766f59a135ae9ec49e359e8a640a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5104756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab4ed3739991f0245817a8ea11bf0baf308bbbc508ea3e644b2d650df9321cb`

```dockerfile
```

-	Layers:
	-	`sha256:f98bd96592c0131ba7887d02ef4cf6a242327364adf8ac7fa3159aa7acfe30b9`  
		Last Modified: Tue, 13 May 2025 18:46:05 GMT  
		Size: 5.1 MB (5090422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1daabc892a0400ce31f0b9f94e389d98ffbeb289f442f1263e17afc19fed70b8`  
		Last Modified: Tue, 13 May 2025 18:46:04 GMT  
		Size: 14.3 KB (14334 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; s390x

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

### `clojure:temurin-11-trixie-slim` - unknown; unknown

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
