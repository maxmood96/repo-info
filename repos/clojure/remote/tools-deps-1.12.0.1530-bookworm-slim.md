## `clojure:tools-deps-1.12.0.1530-bookworm-slim`

```console
$ docker pull clojure@sha256:abd0a1fd97bb6f2e6e6580d00b01373ee48ed9f5c1a00a2893a53870659909ac
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

### `clojure:tools-deps-1.12.0.1530-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:30f88963ce7f6ed466cbab37800309fc91f227c25311d30736b68dbe4e22b169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255388687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6dcc8c12cb84809b77df9cd524c96a839ab61d3f668527afa5709473dd3063`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa70317dd6396cacc011b4373d753fa50d77879e2ef781bc76f1b9269980f58c`  
		Last Modified: Mon, 05 May 2025 17:08:27 GMT  
		Size: 157.6 MB (157634443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02cb0809e8871baae787083ac407b7a3ff52f0edfd73d4e01abb5f393f1b833`  
		Last Modified: Mon, 05 May 2025 17:08:25 GMT  
		Size: 69.5 MB (69525564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1ae6714018e698aa47239d55c20d52b55777b5d51553fdf42f6d7dad558406`  
		Last Modified: Mon, 05 May 2025 17:08:23 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bdc6e9c742e7ea36e5c4eea7ac589d8c0d3c8aed06079670b7452fb391f6ee`  
		Last Modified: Mon, 05 May 2025 17:08:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8d7944be1e5c6d4a9a2c0a0be9f787a5da289a664c6bbc9b1e5dac914b11a998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4934338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3096bece6e395e9aba56f656bcf51a23b8aa4261af19dad4aa70daa104b737a`

```dockerfile
```

-	Layers:
	-	`sha256:b1af8e8b86cc89d6006a8f74636f3fb3878ae6a738c571307d304031047cafc9`  
		Last Modified: Mon, 05 May 2025 17:08:23 GMT  
		Size: 4.9 MB (4917763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6441a1f55cf92ff95e6320a201bad78494f0d26816e833aa18fcabf5395ca682`  
		Last Modified: Mon, 05 May 2025 17:08:23 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1530-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:da151074957b3cfd4dc9ad4683aff18cc6dc464a7b60336892bbb1638496096f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253374076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cdd13af39dca5d58cba939e20318477ea230531391955c71d91bdccac8b6e7b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4ab5dd15c9d773ed92bfed06df23b5bcc8c8b6efafa0f418a37de8edda2a2b`  
		Last Modified: Wed, 30 Apr 2025 01:45:46 GMT  
		Size: 155.9 MB (155928800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93dce20c11a482f6fb2834804f51a6cd619fd60f347512ce5eaeaf1314b6ca3`  
		Last Modified: Wed, 30 Apr 2025 01:45:44 GMT  
		Size: 69.4 MB (69377615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9f1e67364d37e01aeafaaa5af118bbb892edfc55e0f9da469854ccf18bfef5`  
		Last Modified: Wed, 30 Apr 2025 01:45:42 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c0ca1b3269a20507089bccf30eba55beab51bcf6c41055a41eb8481ca2497f`  
		Last Modified: Wed, 30 Apr 2025 01:45:42 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8a44b621b79e8b47f449619de0465a6c0bec6f4f2a79aa4976b261a79fa768d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4940265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:462f800a4e6e207157b1e95bbdd9f524e432bcc86544f67678d5200b867f61bf`

```dockerfile
```

-	Layers:
	-	`sha256:c4b704625b159be4db6d93fe4dbe67718f6e4e011e1e22ec1d9fd310da5aacb6`  
		Last Modified: Tue, 06 May 2025 00:44:18 GMT  
		Size: 4.9 MB (4923548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba381f55ef0393554239a17bbbc4194163ac0bca3e0ffcaf306ae0e0534ee117`  
		Last Modified: Tue, 06 May 2025 00:44:17 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1530-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:870a4105570345d24fac35fb1ef6814935ab86aabefd60f96485a1741e1cfe92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265219191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4911092a6ca837e9deae63c21cc4ccd5700e507dfc88c35a16b1d45518eb9f85`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c25f006c8da87634b15cd9ff02661544ef2e79e4d05effbd9011c7add02414`  
		Last Modified: Tue, 13 May 2025 19:11:46 GMT  
		Size: 157.8 MB (157804905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9f36d96a1a1f25001324066e65ae78670ac3199847ee6e655f355e1bf729e1`  
		Last Modified: Tue, 13 May 2025 19:22:27 GMT  
		Size: 75.3 MB (75344800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5330057daac8d954d9c3dad23ffefe0d30e07fabad448cf31c7c05990005b3e`  
		Last Modified: Tue, 13 May 2025 19:22:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e095547b249d76a3118e38218c91d56eca41fd05b6f7a7c56a57b62ee192314e`  
		Last Modified: Tue, 13 May 2025 19:22:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:80d4ba771aecc72e6267e368d4b79c987309e3f468c2efd9d08d5ada2bce79f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4939402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e48ab9887236d04d547adfdd49b5be4dc019db280d30b24f552cef791b7ffa`

```dockerfile
```

-	Layers:
	-	`sha256:c76f38ad5d36846e7d14004088b64b714b1dd46c711dc12ad2f866ef38919153`  
		Last Modified: Tue, 13 May 2025 19:22:24 GMT  
		Size: 4.9 MB (4922767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eacec4f081095adb05c3b7b4440913cd2311124b8c5bfd471fd31e870d8ab176`  
		Last Modified: Tue, 13 May 2025 19:22:24 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1530-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:a6a110f97fabbdc44d4419fc95c4a5bba9416ce8159bc2c47933562fc5da787b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242129520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0618ae27e5d1082dc2c6f81519676550dd0546802dc29c25362f8abb396df80`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
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
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f784f7cc999483f4494b3c3b7dfd4ae59543c3b7db7deec44c61e633be996e4`  
		Last Modified: Tue, 13 May 2025 18:22:00 GMT  
		Size: 146.9 MB (146910920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7dc3846385f3f9a08572e4e03f0add4a0f12e29c8d5263bc4030f57d113e74`  
		Last Modified: Tue, 13 May 2025 18:28:28 GMT  
		Size: 68.3 MB (68332691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969511c01c67ca9a83b1bbbaf328d353c60b00f50a832843b42de36977fb233a`  
		Last Modified: Tue, 13 May 2025 18:28:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae6e24901b7b771da18b47eeba202712133bea5473fc8dea65125a3cd240d3e`  
		Last Modified: Tue, 13 May 2025 18:28:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8e514e32ef50fcc4da193406478d96d38d69f77d7b8cb6cacc1a0389c0f245d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc6163ab1cce01be1a1a98638674d262ca40b690dfb164ac61dec6a3668dc32`

```dockerfile
```

-	Layers:
	-	`sha256:b95df3d914c4f9c95c556f116c1d0db77d802b0729b56b6477d07532096618fd`  
		Last Modified: Tue, 13 May 2025 18:28:26 GMT  
		Size: 4.9 MB (4911976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b109c93a486112274cbf7b731e0fbfbea147eceabc582130624fd582944e07ca`  
		Last Modified: Tue, 13 May 2025 18:28:26 GMT  
		Size: 16.6 KB (16574 bytes)  
		MIME: application/vnd.in-toto+json
