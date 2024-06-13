## `clojure:temurin-22-bullseye`

```console
$ docker pull clojure@sha256:f5b37dc167bcf6c094a8a9d6b09d6910e826a36e2dbd0e46d383c5ad475a6db6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:21bfbbe6b5d2c8f16460ca98b9c37700688892b79ac31c35a7a4cda819906c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280632324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0fff06ab57f6825812baf6a854c53ebd12cd918c330962d451d5107d11c14a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f0b16146511ef0af5a59dd0ddfc8c3e89d6dafe6194bf1294f148efdda6a39`  
		Last Modified: Thu, 13 Jun 2024 18:14:25 GMT  
		Size: 156.7 MB (156715524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef40904db93dd936591c4466009349b5b28d33eeb5ef55051c2f8c137861ecc8`  
		Last Modified: Thu, 13 Jun 2024 18:14:25 GMT  
		Size: 68.8 MB (68816565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a27179821dd8ab46d12145d97e9ea7b10dbcb8f7258fac10636a553540f3731`  
		Last Modified: Thu, 13 Jun 2024 18:14:23 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4c1bec799e004b398c4f63d6ed8d979644db774afd7ec236f2197a50713de4`  
		Last Modified: Thu, 13 Jun 2024 18:14:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:64e65e64ec4d5a78ffa16d02865606fe2ce738e5ee9dd254d13047ed9a35fea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7015184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70346ca818c0b104bac262bbc9e2d209c6576df2ad3c05f8ba7a5cb7973a8cc1`

```dockerfile
```

-	Layers:
	-	`sha256:cce667bf3bbef0ed94660ba7b6f57fb99a3040e49d812a20e514d682bd149bec`  
		Last Modified: Thu, 13 Jun 2024 18:14:24 GMT  
		Size: 7.0 MB (6999745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa26b253ff01898e40f46f12408f3402e518917927cb36e493c0e175a97afad5`  
		Last Modified: Thu, 13 Jun 2024 18:14:23 GMT  
		Size: 15.4 KB (15439 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:69ac6dd673c6cdac6784807c1ce6adeea8ff9e4998599b08b0836a16f03a94ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.4 MB (277407675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51f03b70dda7dbc7a5cfff3efed017a7bbf5edf37dc924291248dc8f03d43a7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d963a96394e2a9f4df474372727ed0b58c4b095d7c668d6d92d142be8c953f6a`  
		Last Modified: Thu, 13 Jun 2024 12:01:27 GMT  
		Size: 154.7 MB (154738000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2326b0c8327e1c12f1d945ce82bdfc15a6a63ec380d731fbd8bd97eac0ecc17a`  
		Last Modified: Thu, 13 Jun 2024 12:04:48 GMT  
		Size: 68.9 MB (68929046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cebc58e1f7350a38d4948317a9ead896de7164e1a067d7749231196af56ba52a`  
		Last Modified: Thu, 13 Jun 2024 12:04:46 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75600f3cbe00f39734bca9007d468e47515e0fd217ffce6a600535efc0284e8`  
		Last Modified: Thu, 13 Jun 2024 12:04:46 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c3b1c49ea70e0d0b3ee3d4617c2ddf5ab41b30401fe63d49fa32ca7e5f0978f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7021442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b32164dd92e21ffd462033307c7417d1e222d47e8572b6c060f43fedcb3b6fa1`

```dockerfile
```

-	Layers:
	-	`sha256:8a522f64a78a9681f717e9702d51a9fa56e35c296cf45b7f3e4f54716e935f74`  
		Last Modified: Thu, 13 Jun 2024 12:04:46 GMT  
		Size: 7.0 MB (7005467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87f433b709a9900fbc8ebcfe5628182f81d489ccbaa3724212312d7f7d4fd7ee`  
		Last Modified: Thu, 13 Jun 2024 12:04:46 GMT  
		Size: 16.0 KB (15975 bytes)  
		MIME: application/vnd.in-toto+json
