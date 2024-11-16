## `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye`

```console
$ docker pull clojure@sha256:31409f93f1bfae454e0993b225b3977e51b157ec7ef2417424beb4ad0380e1f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:3c968917c17dd6b7071266a50bfc0ebdcf31ce08304508b91e990485973bf0f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268786048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e2ec297c8b5a102a564e79caf07c46e7ba4924f10ced54bdb458f96e71867f`
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
	-	`sha256:f94461e3ae2b8b38fe1abb59368060918b007f1d298feddebe49cd5eacf83fa2`  
		Last Modified: Sat, 16 Nov 2024 04:50:14 GMT  
		Size: 144.5 MB (144536720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a0f9463fd1ef0edf9bc0fab840364163cbdba8f6e867c16490b47a1b9185b7`  
		Last Modified: Sat, 16 Nov 2024 04:50:12 GMT  
		Size: 69.1 MB (69139509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f865c53246b005b14f85208c22414bfad6bbecba561804d71b9d73de707cd25`  
		Last Modified: Sat, 16 Nov 2024 04:50:12 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b84eb3057a68d67fa8015fd3d16829113cf8970ee44395568eb33b8117e4205`  
		Last Modified: Sat, 16 Nov 2024 04:50:12 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d42f69e8038280a4955cbd53d404995247f8b524cb35efb12b2c61499f30746c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7231691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03782080d1e92d41284e6e3919040a2fda5d57b5b6267f988bae25ed57bac8ae`

```dockerfile
```

-	Layers:
	-	`sha256:4362a4cc058317d982ee4897a57b179cca97230aa40a67e6fdcc111d94f0da27`  
		Last Modified: Sat, 16 Nov 2024 04:50:12 GMT  
		Size: 7.2 MB (7215870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efbb6f5e89e581596bfb5dac553571aeee8cb71a3673fac0364af5a73f5f3d58`  
		Last Modified: Sat, 16 Nov 2024 04:50:12 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fffdd9e45a9bd50274c7d54a24c4eaaab5fea9c9a0a4927184020b12ba00172b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266395520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6d66dd106b5a2fca9fa20d840123c4aa14505b165035925dc7450aadbb72ca`
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
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846c0aadb595ce3dad22540ca4af2a416640bd8bf2e148722e96bb420bc4db90`  
		Last Modified: Sat, 16 Nov 2024 05:30:57 GMT  
		Size: 143.4 MB (143360999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4cb1b100c76f899d6361911741b41c072805ad3bc8f02790d2aea553e8173f`  
		Last Modified: Sat, 16 Nov 2024 05:35:16 GMT  
		Size: 69.3 MB (69276407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb69f1d3047b9c243669b08e512b1a3649c04fd758a3dbb2a339f2eb4c4e168`  
		Last Modified: Sat, 16 Nov 2024 05:35:13 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bad2bf11153c74f5206a11c815d87be9f64d02f877d62ceddd6bafe2c0bc9eb`  
		Last Modified: Sat, 16 Nov 2024 05:35:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a16f7c65006028580f1f00af2b901768d82edfa7e16cee43a83f941c244c49fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7236912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f08f18580b976d30927faede3ce2bd59cc1df44ab72ea5270a8392af8b03b9`

```dockerfile
```

-	Layers:
	-	`sha256:db999ea0887a991ac3617e9299a57c76adccfcbb91658514ea9df1bfd0d953fe`  
		Last Modified: Sat, 16 Nov 2024 05:35:13 GMT  
		Size: 7.2 MB (7220973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ccf7824e6dc1b9df0b663c6e6c626dbb873cdfd2a7a2842396a2554ad7ffc80`  
		Last Modified: Sat, 16 Nov 2024 05:35:13 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
