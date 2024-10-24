## `clojure:temurin-23-bullseye-slim`

```console
$ docker pull clojure@sha256:7de781119d380d084f320aad25f8c31d5571510c73f40c6271e023e15b5e2f78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c6caef7fc7ba5155b364d0b9b754ab84ee2ac47a78e0f0d71ba1aaaf66e91b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.9 MB (257937185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46449b0e9fab9d3038fe2dbe8e9de8df1e3c0e4f7b9c5dda28bc74adfcf358d5`
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
	-	`sha256:c31b00529f6a07fa13203c73dbb73bf57711d15e799134c92f5b39527478ecc3`  
		Last Modified: Thu, 24 Oct 2024 01:57:02 GMT  
		Size: 165.3 MB (165295127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9ad66f085b36daff02a2bf07175c119ab48a1b352c19517d12eacb56aa48d5`  
		Last Modified: Thu, 24 Oct 2024 01:57:00 GMT  
		Size: 61.2 MB (61212215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d69737b5b608f7b94fc0a9615fbc844fb81b6357ea27337fcb74be951de1859`  
		Last Modified: Thu, 24 Oct 2024 01:56:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4cf1ed5db581f518e5a7a59100d358115e5817553178b09ecf022d2b8ec8f7`  
		Last Modified: Thu, 24 Oct 2024 01:56:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7cb1a45eb844897b21fbd6445ba9a73099bffb94a252123d3014a0ff883f5372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5146047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6e4011e3dbcd14166250aa82afa2e0b89cf9c44058c9881c37f2f12fde08b7`

```dockerfile
```

-	Layers:
	-	`sha256:180f8b786e33a5111d6aa43b46d6972af549ac671a96799e27999b52d13bd6d0`  
		Last Modified: Thu, 24 Oct 2024 01:56:59 GMT  
		Size: 5.1 MB (5130329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c771078377fc2a6b42160dc9424bbff7800fd0970d530d3ad5b5d4ec2a59add`  
		Last Modified: Thu, 24 Oct 2024 01:56:58 GMT  
		Size: 15.7 KB (15718 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d69357eaf9a58ec5bec3b308788893271331a896f392a3776ce6e1c6a5f25e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254655420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82477f6bf4b4e45303bb838d3b8460d23860fa5f66d6683be90f1f0c87a35a73`
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
	-	`sha256:7c39ecb6761d88d6b99bc02593aa4cfc49106954164617203d5d1dc228b3fa4e`  
		Last Modified: Thu, 24 Oct 2024 09:40:25 GMT  
		Size: 163.3 MB (163281827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8c450b434e1e432a9d009d2a61f94487b28fc6c09e1490f99443d1386b33c5`  
		Last Modified: Thu, 24 Oct 2024 09:45:24 GMT  
		Size: 61.3 MB (61296799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbadada6858475dea503a936282d3a892bd6288bedf0ffb14e15629740ae3ea9`  
		Last Modified: Thu, 24 Oct 2024 09:45:22 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bebe4c206cf378ad26722be0d9a1ee83f3cc59205db4bca2f03bc6227dd6405`  
		Last Modified: Thu, 24 Oct 2024 09:45:22 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1bb286aa77ef7083ac5fb276aa08509afa6d95c72a06ae9ef26e88c36abce444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5151274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda4e45c71a38106e49cd736589aeecc10e3372b3ef920b1407ee1fca8b25e5a`

```dockerfile
```

-	Layers:
	-	`sha256:8d4b48200e51eb93df4bf580d0b9ef72981e6f2ac169d57c8d24847f88d004b1`  
		Last Modified: Thu, 24 Oct 2024 09:45:22 GMT  
		Size: 5.1 MB (5135444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75832dae156daac9d9d52a6e9068f8746fa321fe4d2ed8b9b0c575d0749f8d12`  
		Last Modified: Thu, 24 Oct 2024 09:45:22 GMT  
		Size: 15.8 KB (15830 bytes)  
		MIME: application/vnd.in-toto+json
