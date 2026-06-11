## `clojure:temurin-25-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:c1997a9d9b33eeadfb5fd3995148a29c99de022a1301fa2ddcc3c9c8184f9fc2
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

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a0709886042f7ce855d5a9db7198396caf7a15e018564deb4ef08fa3e123712e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191312680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc5efd523934f7d89c67c74e2658f9c25eb1a683d0693631e4449cf77be8f7a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:44:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 00:44:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 00:44:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:44:18 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:21:20 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:21:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:21:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:21:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:21:36 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:21:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ed80d456b1e8dd5d62daa52088a0b5afedde164daa1184a8b63c4355dd1747`  
		Last Modified: Thu, 11 Jun 2026 00:45:03 GMT  
		Size: 92.6 MB (92574564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4262ed8528f533be3bad7c594bdaf47250d6a9d633fb79c30472802727742e11`  
		Last Modified: Thu, 11 Jun 2026 01:21:52 GMT  
		Size: 69.0 MB (68951665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1751d2ff587437c2a7c212b3f404648817d812a058789a718ba932cc4a51986`  
		Last Modified: Thu, 11 Jun 2026 01:21:50 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3070a23f3572cc76a49901dda82a5aa61e656fbca08d35d3299e0c16edfeffd`  
		Last Modified: Thu, 11 Jun 2026 01:21:50 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a1fbbed31de15417c810c3c7e44eb14535312b540eda34f35fa9453f2c547fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5241018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d926d24d441e72b9c1c31b260a65109ab45ffe52acb9da062658b7447b81599e`

```dockerfile
```

-	Layers:
	-	`sha256:7cb6f7769878fe5b2f5875444d78ceec070511e263db65761342fc31952a91b3`  
		Last Modified: Thu, 11 Jun 2026 01:21:50 GMT  
		Size: 5.2 MB (5225324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ecc31ffaf62959393448e88cb7f285a4344fe572211bd2c794c4761f29f158a`  
		Last Modified: Thu, 11 Jun 2026 01:21:50 GMT  
		Size: 15.7 KB (15694 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7395cf926db3b8a51a568305ba4cd8ef556e0d1ea4179d7b92a4de532f814075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.5 MB (190469275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f04e062b7d196021b538e7a86332d0f4e5af8ca30216a37f66ccdbd85bc5a1e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:25:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:25:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:25:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:25:19 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:25:19 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:25:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:25:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:25:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:25:37 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:25:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d3cbd7ba51177a7e231b22989bffae6dd505369ea668c5be9b79202edf4c57`  
		Last Modified: Thu, 11 Jun 2026 01:26:00 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbaba5a59f78441cc0b53d0b6b32a5216ef9be9458dd50db8d1ea0b6eb6eb868`  
		Last Modified: Thu, 11 Jun 2026 01:26:00 GMT  
		Size: 68.8 MB (68777450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89a1ec589089f2d905bc0caa90c36ad26a97e13b798eb6e45a6f53e6ac9b7fa`  
		Last Modified: Thu, 11 Jun 2026 01:25:55 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611ccaf2a57382cfccc7fefb2a40082671fd40edaa3afa50e45a59f38749cc6d`  
		Last Modified: Thu, 11 Jun 2026 01:25:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:71a455534fb2b865ca13b7271a3ec442095d09fa3afb45d6f0d500a11abdda12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5247895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1969f161bd608fdcdc4289a80825845b816a89e658851ab34b211003dda5764`

```dockerfile
```

-	Layers:
	-	`sha256:1f95045f8b1b8df71ba48945f76c64f7e71528b3ca177121c83ba9f155e10304`  
		Last Modified: Thu, 11 Jun 2026 01:25:56 GMT  
		Size: 5.2 MB (5231106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85f341dc0e314b9279a85847e4b8ed268e0c08d441df1336a20a07148ba3b1f0`  
		Last Modified: Thu, 11 Jun 2026 01:25:55 GMT  
		Size: 16.8 KB (16789 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b9f3377d9252bc1f7e9299108913471048276587aa4261dfc3b1473d6a61ef21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.9 MB (199884519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:436ffe2f2c10a4591721a6d4414bbe40a1e150da2ee1c6c64c070f3084900c0c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 18:07:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 18:07:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 18:07:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 18:07:57 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 18:07:57 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 18:08:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 18:08:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 18:08:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 18:08:46 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 18:08:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182d622beec6c4387449420f7de969ccad2b0cf20d00ff972fd1e3f0e33a65e8`  
		Last Modified: Thu, 04 Jun 2026 18:09:30 GMT  
		Size: 91.9 MB (91914038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0778cec8ae24ac85c06b6eddf4eb93507f3323644c73533d352c489337c88607`  
		Last Modified: Thu, 04 Jun 2026 18:09:30 GMT  
		Size: 74.4 MB (74368984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f241c7541816eae6f16485ba845915b87ff4d38a943c6396034a157c8925b6f3`  
		Last Modified: Thu, 04 Jun 2026 18:09:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd76ead74be20ee7b20a3bc8ca92c53a439feb85ee30674f3a54f54979483780`  
		Last Modified: Thu, 04 Jun 2026 18:09:26 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:797941ed824b614be4bc47aef08949ffefbace0c2d705860945cf2fc1c4f389c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ab5b2f3d563b88b7977060a7cda0c69f43ccc165b07cd70ba3d778807586e5`

```dockerfile
```

-	Layers:
	-	`sha256:882ce7216d02789e582de90a808f88d5d6d800fa014e3d4713003bc54b6867b0`  
		Last Modified: Thu, 04 Jun 2026 18:09:27 GMT  
		Size: 5.2 MB (5213019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b39d04d772def1461c1468a0289fcfd366c41ca936971e5fb3cc51bd63c7e17`  
		Last Modified: Thu, 04 Jun 2026 18:09:26 GMT  
		Size: 16.7 KB (16707 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:603caa09af6946df99e46ba67558d5d822a603299f13c6dd19afa53018971eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188205240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af32fd51ae1cf8aa622f7b5945f028c2f6e9e2dc51e93492aed272482eee62c9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 03:15:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:15:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:15:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:15:18 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 03:15:19 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:15:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 03:15:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 03:15:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:15:36 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:15:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5259b384b4540e6742422b0eb0bf16d13e46f00ec990666d1f48f2dad4c9468`  
		Last Modified: Thu, 11 Jun 2026 03:16:07 GMT  
		Size: 88.4 MB (88420320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b231a08f12a9632f30382835ac865e1fdc766addfef25e37d249eecf9578b104`  
		Last Modified: Thu, 11 Jun 2026 03:16:06 GMT  
		Size: 69.9 MB (69932528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934a1d993a06b6f1683d24e02f54fcabe176c27e79ec0e5f1bf0bceb5ff5ee95`  
		Last Modified: Thu, 11 Jun 2026 03:16:03 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224fda411e86681604350da250cfd6e608deddf2dc3521a68d74c1c0050dac77`  
		Last Modified: Thu, 11 Jun 2026 03:16:03 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b7ac5ed1234d103b29a4bdcf1c44987a9914ede4f70f7787429b7fe3ade69a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66890011fed3ecaa2b1ed7c019e5a69d969af6b5a724aa40aa447d4ab2c7e8bd`

```dockerfile
```

-	Layers:
	-	`sha256:ea2f0d3e798c08dfe62679a29b11d39512584285a5c12399c2da0af7aec7f568`  
		Last Modified: Thu, 11 Jun 2026 03:16:03 GMT  
		Size: 5.2 MB (5205810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5378d97690b713fe8ed7cb23cea362ed3697dfe0d56521b177f166bc4dd6a3ac`  
		Last Modified: Thu, 11 Jun 2026 03:16:03 GMT  
		Size: 16.6 KB (16647 bytes)  
		MIME: application/vnd.in-toto+json
