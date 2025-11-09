## `clojure:temurin-21-tools-deps`

```console
$ docker pull clojure@sha256:0f9e75e288048ff89f3a29c198d8ad321b686b5f7728bfad764a414b62837b12
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

### `clojure:temurin-21-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:7db2d2445dc75172ad684159fca33dc5b91f15c59ecbe0b33e1c6f9559f98f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287455883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0392e6467cce3816cb0028577efa513cdfe42df460066c846e30ef9bcba8d44d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:44:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:44:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:44:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:44:48 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:44:48 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:45:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:45:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:45:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:45:03 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:45:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edad822abae5104ee9ddc5c14e13d21593674a2e6b4bb3638b63a4db36c1b001`  
		Last Modified: Sat, 08 Nov 2025 23:29:45 GMT  
		Size: 157.8 MB (157825975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed74434a7ebe223c5d3696bac4efacdeb48700f5d352101cb6360b1c3d4cd29`  
		Last Modified: Sat, 08 Nov 2025 18:45:40 GMT  
		Size: 81.1 MB (81147809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0145594b750f747adeb19ebb6d1cb934f4f9a18aa0fdb4a0c47e96ffd29aba`  
		Last Modified: Sat, 08 Nov 2025 18:45:33 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af7f197a06b623b000d7da703041909f62cc31631fdcde5f5724cc4277e08ff`  
		Last Modified: Sat, 08 Nov 2025 18:45:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:8916b891f7311215875756ebb7616a88c90f9c5c3fbcf06a1e9e0cbdef55decb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c59127777c65329f4408daa58d83c3eb53f3d001d220f54e09dc0303f2d56bc`

```dockerfile
```

-	Layers:
	-	`sha256:4ee1cb9aff7ca64af4c07b4aa96592c3e9e7c6433d8493002861d4f8b5505cb8`  
		Last Modified: Sat, 08 Nov 2025 22:45:58 GMT  
		Size: 7.4 MB (7378678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c732e49534a7bbb1d905aebafb4b7dd40a089ca8b32e862324c9fb67aa22226e`  
		Last Modified: Sat, 08 Nov 2025 22:45:59 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c672482709a33f864d5acf66465856e5cb8ad7be8bfde512896a7ed515a2ada4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285499026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36aab2d6decee35c9b17788c302faff047670c67d78dd2c2114efe0e80e8859`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:43:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:43:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:43:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:43:59 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:43:59 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:44:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:44:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:44:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:44:15 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:44:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9defc4f2cd147898542a776a6853d1a1f802b01559aaf44a50f9c909c017be01`  
		Last Modified: Sat, 08 Nov 2025 18:44:41 GMT  
		Size: 156.1 MB (156107602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbb3bd089a7d8323c7d715139d0ad0f0b658b7d2f20bdddace41fda708cadce`  
		Last Modified: Sat, 08 Nov 2025 18:45:02 GMT  
		Size: 81.0 MB (81030908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bb0b1b7b25296a0680015122c44e268a631008f0631b54426f52ff8d43c039`  
		Last Modified: Sat, 08 Nov 2025 18:44:55 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd9b5d208d4c9c773c2a0cb617327fd90e2eeb961ff424f5b8f77f47ae35f04`  
		Last Modified: Sat, 08 Nov 2025 18:44:55 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:4abba77b88397413911e9bd7ef03ec4367126d798b836e0fd33bf31d5efb85e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb00082e0f9216c7fb2ca668d6b7c62d82f79cf8117753f27e0b0d0072b7c9a`

```dockerfile
```

-	Layers:
	-	`sha256:3c9c831624d6f3f345ad05761eb93a7d8d76a0c2d0259b5a18f774542c7bed91`  
		Last Modified: Sat, 08 Nov 2025 22:46:04 GMT  
		Size: 7.4 MB (7384465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:087583d2768bd7b1a2e080e8a05b9ca5aa7ac92df8ca1da48e93d260193eb999`  
		Last Modified: Sat, 08 Nov 2025 22:46:05 GMT  
		Size: 16.6 KB (16602 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; ppc64le

```console
$ docker pull clojure@sha256:17046d8a12ae2ef35c8952c23ce6ccea9652417551e2e0b43ddd3d4feecbe14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297257422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d052781d31f5274a3da26d76356bbfa2849547e48f394ce91a6d03cc1c78bff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 21:30:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:30:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:30:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:30:07 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 21:30:07 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:38:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 21:38:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 21:38:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:38:25 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:38:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df5ddb30da5ca300b505c1a0ec8b4685bfad9925d2d21e6e9d69e16d2ad89d7`  
		Last Modified: Sat, 08 Nov 2025 21:31:20 GMT  
		Size: 157.9 MB (157942894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5524c4c3df17f9e53da208b38723eafba630f8b42900118ab5849ba245f42d8a`  
		Last Modified: Sat, 08 Nov 2025 21:39:15 GMT  
		Size: 87.0 MB (86986206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44934b50dce801c63d8b1fdb255bf7f75557a5d1af203f041be736bd8d77f53`  
		Last Modified: Sat, 08 Nov 2025 21:39:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f25a95d425a6d747ef74344b16bb695edbadc474ae00dca08af14ff2696ac2`  
		Last Modified: Sat, 08 Nov 2025 21:39:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:68d76d48c2ca956618c243a69ee9d990b12b3415873ff4e178544d73f8c62128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2def9be1c873c78d48b8319f1eceef80e8f08c12c7b2a8374dd6dbff3dd9ba52`

```dockerfile
```

-	Layers:
	-	`sha256:30de8d4bdcf5817c619d13d404a8cd1cadc0cddaf992da3509521b174330f5bb`  
		Last Modified: Sat, 08 Nov 2025 22:46:11 GMT  
		Size: 7.4 MB (7383904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:983ebd6317f0893ccb8d85df5b338ec2c7c79b3b37413807c305ad4de5f20797`  
		Last Modified: Sat, 08 Nov 2025 22:46:12 GMT  
		Size: 16.5 KB (16522 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; s390x

```console
$ docker pull clojure@sha256:8518f283aa11213aa7c037ff5667323c65c53f16e5be1361ec53cbd9285821d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274165494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6fae92e9392335e8336d329df6a4fbcd72d259f633163bfbe27cb49faa176f4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 20:27:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 20:27:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 20:27:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 20:27:39 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 20:27:39 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 20:32:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 20:32:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 20:32:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 20:32:34 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 20:32:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0f1ee657e8017424c330ba8e64b9a2f627fd4b868716547a5d0262191fd498`  
		Last Modified: Sat, 08 Nov 2025 20:28:18 GMT  
		Size: 147.1 MB (147069874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92a8dd0cdb58ea7ec572e5f63fd79fc62143871a7dd1035445d6a5521167bde`  
		Last Modified: Sat, 08 Nov 2025 20:33:09 GMT  
		Size: 80.0 MB (79956484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7f0d05dce12d1765aa07fb4b79ff3fdba90d9de6aa0f9d2171c52d0c863347`  
		Last Modified: Sat, 08 Nov 2025 20:33:04 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7ecb5c15ad44b953d76bd577d86d801cc294fb3a035960e59b14fa9e7ffa73`  
		Last Modified: Sat, 08 Nov 2025 20:33:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:3d12b65dd68c2e68d88d44a5e93a95484a09f51948fea1ed218abe97c4f8d02f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7386459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb9c95c26c0586a720d78def1ad48b30586146ce6bf542cb9ae1f625b2f46a1`

```dockerfile
```

-	Layers:
	-	`sha256:3d3ae3dbb86dfb35f82b4addc8dcb8a929185fd2db041594e372a3928d9663ec`  
		Last Modified: Sat, 08 Nov 2025 22:46:17 GMT  
		Size: 7.4 MB (7369997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdda5448b115005f6f5d90307a19ca08497157c43f1d68af9a099cbb5054d743`  
		Last Modified: Sat, 08 Nov 2025 22:46:18 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json
