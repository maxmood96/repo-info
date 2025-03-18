## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:35b125b3eb0c612b41d18d667da0626ec0b5aa0f2475a8ac6b58c6b414ae73e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d23ab8273bb37b0dd1a30dc09f0c76cdda8949cd047b6f446a3ff7ff7941f0fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.5 MB (267492190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9eb0483074af8888cd5820437fa687c642d6a4ed76c3724017dc8f4b29f961`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8d1bfb80edb9306e3de72f4095daeae4c281712482255562f2e236ae85233e7d`  
		Last Modified: Mon, 17 Mar 2025 22:17:19 GMT  
		Size: 53.7 MB (53741275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d18b9e7387655c5e52d27612420055e3f6e508fcb878c265cb8d6385f93a53`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 144.6 MB (144566551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d992d37debbf9e07a657fcb1e373dd1f4fa73a807648f5011f4eb522844b02f5`  
		Last Modified: Mon, 17 Mar 2025 23:18:00 GMT  
		Size: 69.2 MB (69183322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc9182ebc3da4c15ff6a0c43dee5fae4a2a41235836f2f3f87c48746eca61ac`  
		Last Modified: Mon, 17 Mar 2025 23:17:59 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153b1bf554b06c859b009005c898fb0c5e2285f640c4c79ea500de3381598c83`  
		Last Modified: Mon, 17 Mar 2025 23:17:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:31cd3fdd88ef3d2c232139e8305a6250cfcf4f6ac6793cdab961348e97482501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7220375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010f1804e85a1e1904ada2daf810cc3b7d8634d25ba15c59e3f456a490413040`

```dockerfile
```

-	Layers:
	-	`sha256:7e1dc735e5c66a6826a92d7218e029c485b535b7eaa176808de58eb5045ba057`  
		Last Modified: Mon, 17 Mar 2025 23:17:59 GMT  
		Size: 7.2 MB (7204555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a9dd6a4500b3b0e900049c9546c7e3c1cdcc5f7adc2157c69263e52a3c3f32d`  
		Last Modified: Mon, 17 Mar 2025 23:17:59 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e730f54edb093ac35aeafe972e1b4c7bb5db88a96cf72b3035891aa9c5c19d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.0 MB (265009712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b16a71b6c18bcd6598f65952614743aae08ff6dfdfe1018c7c7a9c121b47e6e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac5f7c6c7c6220bb5761ec89c55fd2dae4d63edf89128d22e1e53d7cf650eab`  
		Last Modified: Tue, 18 Mar 2025 00:00:21 GMT  
		Size: 143.5 MB (143454700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba669108d3225511d85e8a7b4114bd355617e38fd3d3faf2d0c6c6f2155fc95`  
		Last Modified: Tue, 18 Mar 2025 00:00:20 GMT  
		Size: 69.3 MB (69305579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7739b9b08896b5308920fc4baeb878f62bc396c89a0a9efc988ec46587f4b9`  
		Last Modified: Tue, 18 Mar 2025 00:00:17 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddea6b727b379b1dd392fbb22b54f9cdbaf3445cbda0b5c3ed371f1809cee2a`  
		Last Modified: Tue, 18 Mar 2025 00:00:17 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f162610a6368b7112e5f42b881fc445792f2f777b6c6a7baac9f557e3a5f4c55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7225592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b48f1b8533a4b9a8b9f372fc3c94265e7580c48f366aa55f2e15fcfbeb2016`

```dockerfile
```

-	Layers:
	-	`sha256:4b40147a6607903040fa0f652ecbb2f5dadae845a6cbfbf0fc20d4403fea1615`  
		Last Modified: Tue, 18 Mar 2025 00:00:18 GMT  
		Size: 7.2 MB (7209654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7968c306ee3c6fe07b9fcac9a3000e3b11707906cf633b79e1f22086aad0123`  
		Last Modified: Tue, 18 Mar 2025 00:00:17 GMT  
		Size: 15.9 KB (15938 bytes)  
		MIME: application/vnd.in-toto+json
