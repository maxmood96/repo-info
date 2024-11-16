## `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye`

```console
$ docker pull clojure@sha256:36e00b94264476975dc9bd85f8be12071c36c19cedf7f75158cffcc2897e688c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:2ba2c1dd83eb10250c9f788dc05b74095148e3c72cef710ae6af6147305f539b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269849705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f723ba2da25117025345ad498fc0d2fd51c9bf6a5da86c6346165f5767922a09`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0827ae6c27d619495ee4cfe77ae9bb027b38b2be8f3e6c1e9df1060bec55540`  
		Last Modified: Sat, 16 Nov 2024 03:51:46 GMT  
		Size: 145.6 MB (145601398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b718d9511a2ef5010365b5ad21acf4f86c24640636560886ca6b153debf26d6e`  
		Last Modified: Sat, 16 Nov 2024 03:51:44 GMT  
		Size: 69.1 MB (69138885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e380a9a659659fa26cb487eaf849a0d5597c16a5f1df7e7516808e3722690cc5`  
		Last Modified: Sat, 16 Nov 2024 03:51:43 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7269f4ebc512cf874e8fcfab365f6a388057780ba38667bb1dc72e8a8f1eb6a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7250293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af539bf864f3e42d5475295ef33741529fcdb8956868ef8ed0ee57c39e1e5a8`

```dockerfile
```

-	Layers:
	-	`sha256:c91fb8a7fce1d47d7e4508a271ff74b1efaaf9d7ea145d600d2602bf6dd35dbc`  
		Last Modified: Sat, 16 Nov 2024 03:51:44 GMT  
		Size: 7.2 MB (7236041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:647444e65e11b0c029e931f5fb96a348421d6fe90a69dbecf563dd3b9ce1051d`  
		Last Modified: Sat, 16 Nov 2024 03:51:43 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bfa55b73cb50e43991f0e26c7c7afc96e8a321acc8b57ef2912bf844a5d5e8d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.4 MB (265423045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7f885c00c50effdf4b559c353bbcbd6813d73fd511c6520b18ab951d06ccb5`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b743443a1a096d0629648e4cfbd30aaf2d10c0638449f9ec92bbfb798dd4a2bf`  
		Last Modified: Sat, 16 Nov 2024 05:22:06 GMT  
		Size: 142.4 MB (142389148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a134a5935304590920d7cae3d7c2a44b1b93864833658cf703ddbe9871e914fa`  
		Last Modified: Sat, 16 Nov 2024 05:26:21 GMT  
		Size: 69.3 MB (69276181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3661dae4fc6bcb59932aa19edd64be5db245441f72e156ed06e62ac216afe406`  
		Last Modified: Sat, 16 Nov 2024 05:26:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9fdec3cc72a05ccc46f1b74c62278e5a9122e329f72a16f9be8e235e84038cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7256133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8929b8850331f1d16a6a56fbdef082f365fbd798e907ad8db3075b807ab4f954`

```dockerfile
```

-	Layers:
	-	`sha256:212927354aa9445f705c48f5415447154592398868409f50d1dfb7caef292316`  
		Last Modified: Sat, 16 Nov 2024 05:26:19 GMT  
		Size: 7.2 MB (7241763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5bed0a690a548230bf2809f5cdf0ea3843ae46fdd3a1d91b90788170bcb34b6`  
		Last Modified: Sat, 16 Nov 2024 05:26:17 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
