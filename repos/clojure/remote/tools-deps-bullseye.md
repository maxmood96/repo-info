## `clojure:tools-deps-bullseye`

```console
$ docker pull clojure@sha256:c792168dc8d6b7b3931ad60b5540e0946136f093ae414657be5f875d553495c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a8f7b27c0c670996f13c6d063468b289ec8444f91bd26ea1cee52afd75bfc5d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282995386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45623a11d14096fe00d3299e67418a1bee3a96577d2c057ec30dc8a82dedea20`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950ad14a837fe19d33a72ec3118b309fca59bf68cc751c8759732f28ce156135`  
		Last Modified: Wed, 02 Oct 2024 02:58:03 GMT  
		Size: 158.6 MB (158579293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd82c5586c97590824758ae5106a4bd9bdaf1daf73ed87d4aed245d6cc8e6b6`  
		Last Modified: Wed, 02 Oct 2024 02:58:04 GMT  
		Size: 69.3 MB (69333663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4774607e295387293cafd6b585d03839e7fda364ef835c92ea69044535bec7af`  
		Last Modified: Wed, 02 Oct 2024 02:58:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea668b8f7460516f28db975507197bdd72bd272aeb66786910be52a678a691c`  
		Last Modified: Wed, 02 Oct 2024 02:58:02 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4739119dfe6f4c83b4764297bdb3997c92cafd5faa0a82604226c8070b22adcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7209901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abaa30212e19b5fab281cbf4724c41351fa9b06fef7a6310ba8da96d98599ec5`

```dockerfile
```

-	Layers:
	-	`sha256:3abaea640e8a20e3be2542220780091804e0e9437604815e6eee60898b5a8f32`  
		Last Modified: Wed, 02 Oct 2024 02:58:03 GMT  
		Size: 7.2 MB (7193780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5295140309981c3700851b8c6033141048da9a415b41fc3cfc3b3a8dbb83661a`  
		Last Modified: Wed, 02 Oct 2024 02:58:02 GMT  
		Size: 16.1 KB (16121 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ecc93bb9717a897f25e4810c09f4549a29ac4c56f1211324f40d69c8c5502eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.9 MB (279947874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69c0ac334c12232790cc1a6a51638745288433114bee916fdb7893f089b17cb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8489597046021c0abe822796a030474fe683a72d6807de0ea28adcea9da2689e`  
		Last Modified: Wed, 02 Oct 2024 05:38:33 GMT  
		Size: 156.7 MB (156746148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58783f52d388d5f1caf8e6386653c1fae797cc82daf55915cfe02f3dd94ed21`  
		Last Modified: Wed, 02 Oct 2024 05:43:11 GMT  
		Size: 69.5 MB (69466822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96999adb260670f3ca67f8a7aa966c85fe717ea58747cc993855ab44e9ffdf90`  
		Last Modified: Wed, 02 Oct 2024 05:43:09 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6543167b6ca4cc9322d8e3b4f62a96300f96ec2bde8c794548f9c5ecaca9d9d5`  
		Last Modified: Wed, 02 Oct 2024 05:43:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:cac8904c5106c31f86013ac6eff063bf9bf9dfd717fbdb637ebdfb581cda504c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7215157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9cabfef4e373c32c647900d858a97150a4aba8839ee50ffc8ac85ca0af2682`

```dockerfile
```

-	Layers:
	-	`sha256:2b6fdbbd5915732d0ea57df67844e2227a2202ffb5e47931138c733cf690e0d9`  
		Last Modified: Wed, 02 Oct 2024 05:43:10 GMT  
		Size: 7.2 MB (7198907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47c9373e8c2631bc4f5513e43f2f00a2767b99cc637b0f6e5e71474a68dbc2f6`  
		Last Modified: Wed, 02 Oct 2024 05:43:09 GMT  
		Size: 16.2 KB (16250 bytes)  
		MIME: application/vnd.in-toto+json
