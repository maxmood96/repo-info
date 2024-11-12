## `clojure:temurin-23-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:080ee988ddb914c3b04d3c3d8085d6eee21612439988f8cdfe0cb0577ab685ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:201b7c950e8d06dc7e2769005e9e1588928b03f4013e1cf1f506969f83713cbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289543514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5109248d140e77a18b45e64eacdabb3164242b6f08285a2c1ea7d5b615096ab9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba7b5d8836ed8bb5c769cce378fa636d1483d73ce9a4ed9d3de7ed704d44d9c`  
		Last Modified: Tue, 12 Nov 2024 02:50:21 GMT  
		Size: 165.3 MB (165295097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85d1ba1637d6bb6338df5ae09bc153086d8451a79d8adb2bd73ed13b2d2cb50`  
		Last Modified: Tue, 12 Nov 2024 02:50:20 GMT  
		Size: 69.1 MB (69138597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216e29e14a0082fb730ca0822ab659670ff066ab4b6fcfe5499b7893a2ce2fc9`  
		Last Modified: Tue, 12 Nov 2024 02:50:18 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f0c37d56e940bf005fa5bf84122202323d6b55a416903ff82c3cc6bfbba304`  
		Last Modified: Tue, 12 Nov 2024 02:50:19 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:5232debdea01d460a733495b2880abeb45fd5108db5e2f8a0059277ab6828ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7236703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd0a7de7e97ad318755903e17d69adb72bc89c6e987ba1ffcfa53c6799fc3a9`

```dockerfile
```

-	Layers:
	-	`sha256:7587080e9cda2107d3e3f17bfb7898b13e8203662549d9e90539ef6009f2f946`  
		Last Modified: Tue, 12 Nov 2024 02:50:19 GMT  
		Size: 7.2 MB (7220883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601ad44f3423715437f3955d1ea252ac1cdeeb9b955ac7e0ee8c4ab582f6f23f`  
		Last Modified: Tue, 12 Nov 2024 02:50:18 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0a856eeb71d5651a80d0fb29c0aa680a17dc13903522530cdc62263ec197dded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.8 MB (288789344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d089e77e15e2c5e5433a547146982bb8973f73ebcf91d365e107faf304640f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
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
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f985f8cdc870263d7c9c2eb30e17d5f7eccc559c94fa90f2ce64fc3cced1912`  
		Last Modified: Thu, 24 Oct 2024 09:38:21 GMT  
		Size: 163.3 MB (163281826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73d45682e07c937796e42c666fa7c5babf18ba7847eb2ebe29d5660aa01f4ac`  
		Last Modified: Thu, 24 Oct 2024 09:44:32 GMT  
		Size: 71.8 MB (71771585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7dcc4d3c30e0858e06e31a63355d8fbac0a5816f27b784185b7b2d671fb8911`  
		Last Modified: Thu, 24 Oct 2024 09:44:29 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b7bc2609ceed5246a62a883b6f124c8d7e94027b02951da9220cdb0a5a2014`  
		Last Modified: Thu, 24 Oct 2024 09:44:29 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d82db14bd2e3cb0285201e679c186abcf9b803a71501f9b6707c08b2eb23a5c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7241085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e47189526ecaba5ae1fd5962da28b82497c4aa5d77ce37c4802dcf971cca36`

```dockerfile
```

-	Layers:
	-	`sha256:822a11b25406672b5a3512d50858a55a233cefcc955878cf948a63945213807e`  
		Last Modified: Thu, 24 Oct 2024 09:44:30 GMT  
		Size: 7.2 MB (7225328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2e22a9bab44a90ee30b654cfce78503a0ca03b7a8b997edabc5665a5c47da9a`  
		Last Modified: Thu, 24 Oct 2024 09:44:29 GMT  
		Size: 15.8 KB (15757 bytes)  
		MIME: application/vnd.in-toto+json
