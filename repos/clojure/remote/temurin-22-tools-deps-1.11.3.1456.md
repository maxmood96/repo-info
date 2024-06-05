## `clojure:temurin-22-tools-deps-1.11.3.1456`

```console
$ docker pull clojure@sha256:4fe2f21a35a5aacff1617834e7261d22ed516254abfc079d12e54cfe130b82fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-1.11.3.1456` - linux; amd64

```console
$ docker pull clojure@sha256:5099aa52770ac8bb8181e4a4ae2cfeee513170e30cb5d96a74bdb9cffb7252f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286592743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5902cdf715b4e9e383e9717ef483261fda9fe82b20219377fd62b6cdcd79b48`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1be7480ff186bf4401710829ce4127dec1b7668bff4ba09be1c74544c46961`  
		Last Modified: Wed, 05 Jun 2024 06:12:43 GMT  
		Size: 156.7 MB (156715500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebda725f227678a9f452c738618d42700abec6ae13d4f9c2a7fde3e6b020a42`  
		Last Modified: Wed, 05 Jun 2024 06:12:41 GMT  
		Size: 80.3 MB (80299808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54666769fac3162d9486fcc2cccbfa0ab85f1a2cc27a7575caa5f4e9442fab6c`  
		Last Modified: Wed, 05 Jun 2024 06:12:39 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a60b530aeb5f252b8bfc0b1ef127149100ad63d483f5f4357570c773c8fc035`  
		Last Modified: Wed, 05 Jun 2024 06:12:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.3.1456` - unknown; unknown

```console
$ docker pull clojure@sha256:78af58fd60bbb76261c641147fc48cbade8b026ab2874aebaba0f91f7fff383c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6977418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b825970191bd8abc7655d81a54ad441189d9ea91502c810b03e14606a5e807b5`

```dockerfile
```

-	Layers:
	-	`sha256:3c1c7b51c8c630fd511939512b9ba5d17cbc60cad1d415922ffd431d2c7656bb`  
		Last Modified: Wed, 05 Jun 2024 06:12:39 GMT  
		Size: 7.0 MB (6961344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:521010bba5a66b6edfbb63d7ce14b083a1f37cbb6c6ceae409cf96307c2735aa`  
		Last Modified: Wed, 05 Jun 2024 06:12:39 GMT  
		Size: 16.1 KB (16074 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-1.11.3.1456` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8606ff04291ae4f292da3143591dd4229744f55e285db231a41754a4821238d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.4 MB (284397375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa60dd729fdc428edb81c7eab0faebf74a525baf3bf07ae99e4c2b66a4840dfa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108f143689701d7a45796937e60c77f7cbfbb3549865de2a74d02c7a13faa376`  
		Last Modified: Thu, 30 May 2024 01:38:23 GMT  
		Size: 154.7 MB (154737940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4a79e4366c7358c331d29541a6c5f9d5fc83865e249d2787340a9184221c42`  
		Last Modified: Thu, 30 May 2024 02:06:29 GMT  
		Size: 80.0 MB (80044998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdaf1295182ce50043f2b841350b62a7426d1e8d81dcffa7c21672be6ff8815`  
		Last Modified: Thu, 30 May 2024 02:06:26 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810290c97a3b90aed1e7e5f43de2d4ba2d2a47c087faab950ebfd37afe01e3f0`  
		Last Modified: Thu, 30 May 2024 02:06:27 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.3.1456` - unknown; unknown

```console
$ docker pull clojure@sha256:46c4826e36eb1e2fffbdfb62e3845d332f47b1a3a1fe9d9418896c74f7096f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6984390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d82d7f8d1b06e6878a404368323571d6f688f7e52c177f71a7dbabaa369140e`

```dockerfile
```

-	Layers:
	-	`sha256:80c40aa55d6b89319de9514cb79dae55f69e2cbdd3d0445ce2737ceb8285dc12`  
		Last Modified: Thu, 30 May 2024 02:06:27 GMT  
		Size: 7.0 MB (6967756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c564e3952213ef18178b6daa181481796b2030b8f5cb0bef057ad61295f07fd2`  
		Last Modified: Thu, 30 May 2024 02:06:27 GMT  
		Size: 16.6 KB (16634 bytes)  
		MIME: application/vnd.in-toto+json
