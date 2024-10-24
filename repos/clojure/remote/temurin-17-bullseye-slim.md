## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:bf948bb637f333752ef84f3b192b92bc847cde45eb97e8eb579080b41f8aa799
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3c1f04334665229b23621c438b656c6625a77596ef64968f219e146177a767fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237176929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb27e29e485ecd8f763c671a59ebf58beac15f36493aeed61efaf973e1a9a31`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
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
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655004cf4b175db2bcc273867245c753bee16ba55bae840ceb487c0e8bbec6b1`  
		Last Modified: Thu, 24 Oct 2024 02:00:25 GMT  
		Size: 144.5 MB (144534810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da134c56aa810755455a97c4cea7e4a5ccb0b07a885e4de1a8ddca03dcde6db`  
		Last Modified: Thu, 24 Oct 2024 02:00:23 GMT  
		Size: 61.2 MB (61212282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a851775e1e319503f78968066a39fe865b8c6822a25b4f03be05bc14d24d84fb`  
		Last Modified: Thu, 24 Oct 2024 02:00:22 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3337fb166f26558dab6047bcf9ca9922f95d8f4b94f259f9e8b9a3cf1c168df8`  
		Last Modified: Thu, 24 Oct 2024 02:00:22 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cbeb5a7b057da80fe2d46b35b9e6195afdc92be855a27f3f91f04ac7b629e4ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5141035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2accb171eab041c59f4428b11e5ed7a4c1eb94f13e3d0bdb03e6f3d533915bd8`

```dockerfile
```

-	Layers:
	-	`sha256:397640157825e650737aa999b6abaaa326fe079a4c541b1cd096f782549c1b49`  
		Last Modified: Thu, 24 Oct 2024 02:00:22 GMT  
		Size: 5.1 MB (5125316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d402957d3a6bce960cd44c0fb51e9bd911749a1b976b1924361dcc8dddef93`  
		Last Modified: Thu, 24 Oct 2024 02:00:22 GMT  
		Size: 15.7 KB (15719 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d7def7862e08087c3254d8e13a7e61df52e21797ac2d87b68f0d8db04a53f6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.7 MB (234734605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8210104973a049db0c05f87c7b38a619fa7a213ad416e1ec8f83a29b4fb2bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
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
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9573ebf30d84979ab9243f8719a10548944ad9e1c6626c4ec7fca113cef24304`  
		Last Modified: Thu, 24 Oct 2024 03:37:49 GMT  
		Size: 143.4 MB (143360974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98c7227d8b1a4a3b2a9669566eac0ca5ae7405802f9c6d54814d77323c6d28e`  
		Last Modified: Thu, 24 Oct 2024 09:22:11 GMT  
		Size: 61.3 MB (61296836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e45ba11b41ed079b198c05e4ca2af4eda69e37997202a5c3ac3f977f0282e9`  
		Last Modified: Thu, 24 Oct 2024 09:22:10 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa908f4c32395c01379c1537464056e963c1ef3972927fe66cad8a3e60217fae`  
		Last Modified: Thu, 24 Oct 2024 09:22:10 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2a42829a06f995599ca48f6512f901a7293fd8a003a5145cb0072952fc4269c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5146884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6335daae5362217326095cb55e14146bffe31dbfa072110269931eca22d2f331`

```dockerfile
```

-	Layers:
	-	`sha256:f6cfc7c8719a35aacdd0f683f22bdb059c6f0c9341566c93ba4dc9331e2bea75`  
		Last Modified: Thu, 24 Oct 2024 09:22:10 GMT  
		Size: 5.1 MB (5131053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7600fe230715455287bb253181712390e554d7d485a333c1c98fad041032318e`  
		Last Modified: Thu, 24 Oct 2024 09:22:09 GMT  
		Size: 15.8 KB (15831 bytes)  
		MIME: application/vnd.in-toto+json
