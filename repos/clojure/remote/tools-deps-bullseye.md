## `clojure:tools-deps-bullseye`

```console
$ docker pull clojure@sha256:a487027a6d469708b2a376bfd1326ee8202d74abf3172b675c369db01c75f254
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:31f5c2ab08a2e6109bdc85a67c6d6d446d28621ed45b9582737796cad58ff628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282995546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c82424ce42c12c7870bf0f9374b637ee32280b895e867ebb2495958601684d96`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a2fc9f7ad0339df12179491440f7075b3cad747a7067a7ab6e7110b8eb93b2`  
		Last Modified: Wed, 16 Oct 2024 16:13:15 GMT  
		Size: 158.6 MB (158579244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3d340c09557a371ef75a53711f4ec734c93735e2c2937c122350c307d60a45`  
		Last Modified: Wed, 16 Oct 2024 16:13:14 GMT  
		Size: 69.3 MB (69333865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f09f1035fd7173cb6eb4d888ceb5b5920cd626a823db3b2d057c5575e77bd7`  
		Last Modified: Wed, 16 Oct 2024 16:13:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2a28a8622806332ee39fcbe0600d62485f9ceadb94213f0d2c338bab79df19`  
		Last Modified: Wed, 16 Oct 2024 16:13:13 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:28f808d7a6b0db21e21b115996c96250547c1dd6fb377e29cc11f06432cf44e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7209934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c808a61b6ac9eff550a89a7f010afa1933f160d2e987990bc3f595e7a51d2d46`

```dockerfile
```

-	Layers:
	-	`sha256:581331e9d0a845552bf31297a5a263417d6251497a86813dd98bb77fcc5ecdd3`  
		Last Modified: Wed, 16 Oct 2024 16:13:13 GMT  
		Size: 7.2 MB (7193780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe3a540fe76a1f0c7308e065cd448e71f5af0415433391144ad9116746e8ce0c`  
		Last Modified: Wed, 16 Oct 2024 16:13:13 GMT  
		Size: 16.2 KB (16154 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b0b3261e9f39b65952bbf30092e31e6605f97b8c3d0ccb297207e249fb12ec20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.9 MB (279948090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e302a018ffc7ba1395f31516f83829fb1c720ea35900954f635b9ce521af960`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d63d336c3ffd8ca47d040968252435d0359996fc6053a1e58800d5fd2b5675`  
		Last Modified: Sat, 12 Oct 2024 01:23:53 GMT  
		Size: 156.7 MB (156746254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5139e28389b2bb625b715fa416e5591f7e0b2333c6c2008face5e2b6d9860598`  
		Last Modified: Sat, 12 Oct 2024 01:29:02 GMT  
		Size: 69.5 MB (69466929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecec5c43466d5a0f246feecb752c8529782fd551297c4626c9ef65141766d5a`  
		Last Modified: Sat, 12 Oct 2024 01:29:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3431893b8f1e6736cd79acee1794591d9f319b9ced4dc1adc99fc95923f4b38`  
		Last Modified: Sat, 12 Oct 2024 01:29:00 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:60fd248c0bff90e4e10faac7871c9877d022bfeb7c84a17da0e30429390a846a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7215191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6004b013706bfeeaa1d21c1c6465fbbf281675761d09b10f63a9f9ae00204024`

```dockerfile
```

-	Layers:
	-	`sha256:7b488000b8c85f0d41e6d702d1154806fdc13a5a010f4952475710cccf21716a`  
		Last Modified: Wed, 16 Oct 2024 02:36:23 GMT  
		Size: 7.2 MB (7198907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6716c4f53934c2716783beea5179ad64a93c88ff917ae6d074fd5842f004002`  
		Last Modified: Wed, 16 Oct 2024 02:36:22 GMT  
		Size: 16.3 KB (16284 bytes)  
		MIME: application/vnd.in-toto+json
