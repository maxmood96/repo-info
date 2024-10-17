## `clojure:temurin-21-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:42fc3c4cc6170f39f8830a106d0a7a0b807a7c38bb1d09f409aeb434700d5219
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9dc408e3dde9f54fde5e8620bc2499c2dd21e89658257ba6ee88531aa0aa8eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282994532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb893d56bd3d2b4d763d2b5d027fe909f6847b50c20793797ec3694e72a28fbe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Thu, 03 Oct 2024 17:49:34 GMT
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
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47bacd135be2ea749ff6a80b682afd90e4ba1b40a055cba9cc86e9ffb9fdca45`  
		Last Modified: Thu, 17 Oct 2024 01:13:45 GMT  
		Size: 158.6 MB (158579244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0dfc6a88ee4941690933a7c75ac7e3766654d5d49b340159f2cb6f0f422fc0`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 69.3 MB (69333638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79c0f9297b88de4d3aafc0a14fbd83a794d387b4e56824fe65c040eb596962`  
		Last Modified: Thu, 17 Oct 2024 01:13:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ec6a42715d4d976063517940a4995a99555cbeb44b6bb12a051289511ebdac`  
		Last Modified: Thu, 17 Oct 2024 01:13:43 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d7447249abde3e6adcc370d6496758e7dedb75ec914f9178496c40639b4c9081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7210024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7e082b309959f2263dbc257d6b2d64dd7ce3eb6bacd06448c30f32b0b06189`

```dockerfile
```

-	Layers:
	-	`sha256:ee19d10908a8cb04c591238e4d31571ad9c5c08ef79da45e1b65d8e6ffd1a807`  
		Last Modified: Thu, 17 Oct 2024 01:13:43 GMT  
		Size: 7.2 MB (7193870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df835e3ddf02f6b24899ba89fdef24b2eec1451de1f23674b0c133584df4bdd2`  
		Last Modified: Thu, 17 Oct 2024 01:13:43 GMT  
		Size: 16.2 KB (16154 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye` - linux; arm64 variant v8

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

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

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
