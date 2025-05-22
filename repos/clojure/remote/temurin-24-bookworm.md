## `clojure:temurin-24-bookworm`

```console
$ docker pull clojure@sha256:0f3d41579b87433482152e7fe461ffd2a3d5439d518ebaf1e5aa950e729d9835
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

### `clojure:temurin-24-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:19c3ef4d07bc50739da8c87ddd7506d2721c658db63dacfeb7e1e29e3c1c8608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219436228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f181e706e2c6085c025b51ab6063eb23d63d34ad1d7a859c8d752d0f45996c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e9d85acce1b1e0b70e24fa9b0384eb71c85e8baabf82aaaaee60dfed511b2b`  
		Last Modified: Wed, 21 May 2025 23:33:43 GMT  
		Size: 90.0 MB (89951993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca0daac3125bd7082049de50c91f7c0596b9559be312a4c67ad3c86b3ad9157`  
		Last Modified: Wed, 21 May 2025 23:33:43 GMT  
		Size: 81.0 MB (80994953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05acb9336ae01bf445ede0fb018f8fc1e64af16abb6db1e39a766b7a59e5e1d`  
		Last Modified: Wed, 21 May 2025 23:33:42 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c938327c7e8e99819be963d6dc45efdf4aad2830616fb1139005732db310e8`  
		Last Modified: Wed, 21 May 2025 23:33:42 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:10e196209f9f36e6815e500fd025100996adc28f22238f5621cc61145e446217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7186350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91b6c20b12e74f7a16adab49e6306b7bba023e9caa66248404e26c169b68a8d`

```dockerfile
```

-	Layers:
	-	`sha256:c30209ef40d25626f3cc68d6b1551e8308b10347ed83693f7433c7e4e8ecb2b3`  
		Last Modified: Wed, 21 May 2025 23:33:42 GMT  
		Size: 7.2 MB (7169852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af65c28d2d32de294588a1c8ff9341431151d00281f3d3c9d71bf53f739b059c`  
		Last Modified: Wed, 21 May 2025 23:33:42 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2e40befadd1e32e7422707fef1df9e4f34e1a8509c30314cbaab357201dc4548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218266202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf31c2a0499efeb134d4f4f47e79920f039cf33d7ba68a79c87bfa20273108b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf563c5cac7c79ed63b2c1b42791a3b8312c8b10c7a06146f7d4fcdf8c247aa1`  
		Last Modified: Thu, 22 May 2025 08:38:44 GMT  
		Size: 89.1 MB (89091279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cafc858ce99f1cda736c1ba4c1dcbac8aa640bdee8957fbfe758e04c25faa36`  
		Last Modified: Thu, 22 May 2025 08:43:56 GMT  
		Size: 80.8 MB (80846704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d607fb50494214a2f22c902b1b05e2f44265b5b51fb17e4a09fa08ecb463e0fe`  
		Last Modified: Thu, 22 May 2025 08:43:54 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3635da366664dbdc3925bf29963b7c4f667ba1945d1f5bc3fd0cc84197d647`  
		Last Modified: Thu, 22 May 2025 08:43:54 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:dda2b2e62f60586a248c1266aab24e3675d3f4e2cf1118ff0b855c01f5bec70a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7192275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d8c2bf375c0158ac03b45c13aba884d658e2ad2a4ccc905fdda4f4001edca8`

```dockerfile
```

-	Layers:
	-	`sha256:b0fe38e8bebfae57f51ef2b4c8b34b0cc223e834ebbed3393c9aabe658b55a1d`  
		Last Modified: Thu, 22 May 2025 08:43:54 GMT  
		Size: 7.2 MB (7175636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeda8ea4013c915e55f0cfeea38d607125b2a4460c6d3346a6021d8ed9ebba86`  
		Last Modified: Thu, 22 May 2025 08:43:54 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:979af249876412d208ed65c40224ac31da363543b557623ebb895277757a3364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229063079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa1ab7e183b9ac5e9a41f635cddf2de386a82ebbd474a812f2b05d911f7645b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be15ba513f3b44f366cda3823db7673ec6d857c70b5dd1601ee00497ad2c723`  
		Last Modified: Thu, 22 May 2025 11:41:39 GMT  
		Size: 89.9 MB (89920247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e403b9f8db9a8f23bb4bb3da51bb51dfcc3ab19c9e49be87a5a783a6797510b`  
		Last Modified: Thu, 22 May 2025 11:49:01 GMT  
		Size: 86.8 MB (86810171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2b085dff6b315192282ee2cf417e02df0c6b7fe260dd3d9aa425a46e68d156`  
		Last Modified: Thu, 22 May 2025 11:48:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ced57d653c3828e937093f5278c21311a0e7bd154b9039f1777e90ba1a8908`  
		Last Modified: Thu, 22 May 2025 11:48:58 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:305b7ab8fc76b152af6d9a6e7e7efd5bf9acc9b59537099bb9962e795eac0be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7192924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f50542bd2484228a78f4a88989f06f588fe702595201282d3c8ca7d1c5bd6d79`

```dockerfile
```

-	Layers:
	-	`sha256:75063becb4e20154218f376baa04c961fc493ba0e4c34551a524af34c9f06976`  
		Last Modified: Thu, 22 May 2025 11:48:59 GMT  
		Size: 7.2 MB (7176366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adac1d990adb8dfd5fcddee436c3024be26698b746f5e4a53d40a00b206291a2`  
		Last Modified: Thu, 22 May 2025 11:48:58 GMT  
		Size: 16.6 KB (16558 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:0c6457c80adef79834739c76572aa778712f28cbaae7a0cbed49ae3c0bbf3237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212152089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2f519b0f52d5149a7bce4b0494db6253027fabef5d2b37a6b941802b4a1e86`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Wed, 21 May 2025 22:28:14 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b727ee5e72a4360d56bb5e6371b9a080b8c4eb11aef978f2864b9c6113de96d0`  
		Last Modified: Thu, 22 May 2025 04:05:47 GMT  
		Size: 85.2 MB (85216843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0525a2051e19681042d5e035ed4365500e1d81a4a4f8d067ce57eaf3bc8efc`  
		Last Modified: Thu, 22 May 2025 04:09:46 GMT  
		Size: 79.8 MB (79790363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c665fbe0c1c9d207d90b6fa5c3fb369296207dc1276340ee198447ad13df3a4`  
		Last Modified: Thu, 22 May 2025 04:09:45 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d535929abcb38a35d4fc18489741fd1684bfd7c3712dc32fc52f50fde51980bb`  
		Last Modified: Thu, 22 May 2025 04:09:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:eb5c1d8263dccb1ea83153b019a760a4023538e92de7d22de4298b363dcfaf3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7183108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82cb8667905cd507cca40da1661542bb1c225a4656a069300ce3acdc29142db0`

```dockerfile
```

-	Layers:
	-	`sha256:5cf1f9b14eb6c24d5496bfc6dd134b29f84048f2b021ed370339ca2adffca6c3`  
		Last Modified: Thu, 22 May 2025 04:09:45 GMT  
		Size: 7.2 MB (7166611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f1aa703a7ec50c9eaf6324bebba659de8e865229ee7151666c181e826600850`  
		Last Modified: Thu, 22 May 2025 04:09:45 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json
