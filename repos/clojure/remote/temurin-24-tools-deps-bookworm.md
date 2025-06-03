## `clojure:temurin-24-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:8de3e5d41ece9a5107346f50714ec4a3a7925cdfad871f9e847e8f750d36c893
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

### `clojure:temurin-24-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:4dfde9ac48ba8a2451d5df4b552ba8e0f49c3e9a6a52beb3bf8d7159459b6ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219436132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a04e939491c5edb7b001fbbd1dba60297e395e585643f19a4c28b657da5b879`
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
	-	`sha256:a69e5b3af59d596af4bcd7dd8ea3f9776673f9f316171286956d02fc88d392ef`  
		Last Modified: Tue, 03 Jun 2025 05:17:04 GMT  
		Size: 90.0 MB (89951990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2315ba529927164feffa8fe43dd17223361db0034dc471fe1604405611dcc566`  
		Last Modified: Tue, 03 Jun 2025 05:17:03 GMT  
		Size: 81.0 MB (80994857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822145d1a701e54062f13e429b7160e9a034dff685d41314dda280f1b3fe88e4`  
		Last Modified: Tue, 03 Jun 2025 05:17:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a1078909122b67c2d4e1529e59803aff4d159d397da2b608b3ac24dd74704b`  
		Last Modified: Tue, 03 Jun 2025 05:17:01 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:52e6000d52a73d3da575d3b3b515ce106639d0b508dfcf6ad11469705d5cdb13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7186349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca773e530c7418756702864850612ce8b1220aea4c470dc7f181a985ab052d2`

```dockerfile
```

-	Layers:
	-	`sha256:96229c89a68792638bbc7ed574b3e5a72d4828f7ab6f4f1f215beeda743c2317`  
		Last Modified: Tue, 03 Jun 2025 05:17:01 GMT  
		Size: 7.2 MB (7169852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b69e1be3341ba946e609a3f157c448f25d1ae72e4d0626a200550502e80fff18`  
		Last Modified: Tue, 03 Jun 2025 05:17:01 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-24-tools-deps-bookworm` - unknown; unknown

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

### `clojure:temurin-24-tools-deps-bookworm` - linux; ppc64le

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

### `clojure:temurin-24-tools-deps-bookworm` - unknown; unknown

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

### `clojure:temurin-24-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:4f348ff726dcc600f571d99b272383e40c221701e115742af4aa37601ae58957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212151921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f3fb2e487e9a4450082e580609e6d087beb2861450e345f770c6951f510d914`
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
	-	`sha256:14a88af61dafe611dbf396e5a57107bc7b7f88c5b3a0ba26ce314843717b096f`  
		Last Modified: Tue, 03 Jun 2025 06:35:46 GMT  
		Size: 85.2 MB (85216876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65471463aacbf0235e11ab2e00b78d6f9eaafc18c8852541183f5be17b816a94`  
		Last Modified: Tue, 03 Jun 2025 06:40:39 GMT  
		Size: 79.8 MB (79790165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602314353829f0e228f95cb0734ada432ea7b5b94d941b656b2e6eece8d8f4e7`  
		Last Modified: Tue, 03 Jun 2025 06:40:37 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6193d56c0f7c88f252eaf028d00b3c97f0f888e0216b1843d1964056365dd21`  
		Last Modified: Tue, 03 Jun 2025 06:40:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:69ff5dc6c6a73a409ad9a450b6f99bcac72bab1c1023a3b8b22f530051ad4be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7183109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d100db48ddc2f7d6474da14b2e7f0ea0f2b4b0a52c8868947bb1d29faacbb8c`

```dockerfile
```

-	Layers:
	-	`sha256:0ba1b0868bb5858618c2e9829987e8c7c8d2ce1f38e4eaf6ff561d1eaf5b6ebe`  
		Last Modified: Tue, 03 Jun 2025 06:40:37 GMT  
		Size: 7.2 MB (7166611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5894ec35a8c289a5c70d9cc1f5d0c76d2673143b554f6b94ee24355b4175135f`  
		Last Modified: Tue, 03 Jun 2025 06:40:37 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json
