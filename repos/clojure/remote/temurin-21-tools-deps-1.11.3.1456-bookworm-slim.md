## `clojure:temurin-21-tools-deps-1.11.3.1456-bookworm-slim`

```console
$ docker pull clojure@sha256:9b8eb2643107690f3f36801f269a8ee27076215ca57494041d2d4735faa080f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.11.3.1456-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5ae2e5c52583e182df4e4a2e6f53a1a8fa41e063eb452f59c93a9d2f9a00a720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256774196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c68915c8f365ed4bd852eabccbacf4062a29d8ccff3b29505ca132cdf7e1687`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8eb629c064372532104ca9e40763bee03fe4279fd0c7a2109a6b036ffe01bbe`  
		Last Modified: Tue, 23 Jul 2024 02:01:24 GMT  
		Size: 158.6 MB (158579315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b6b2bde7d2e0f5a964926a406ca9b01d54569b3b359f3515cca9133c8e6637`  
		Last Modified: Tue, 23 Jul 2024 02:01:24 GMT  
		Size: 69.1 MB (69067559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2bb0265c34a3b1a5e52edbe7b691eb22bd61983efcb0ccbd1f83b92d17533c`  
		Last Modified: Tue, 23 Jul 2024 02:01:22 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b570a5d16f905f8a15e12b35a739c1ca845af7d24bb9edb9cb6cbc2d4b5c1463`  
		Last Modified: Tue, 23 Jul 2024 02:01:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.11.3.1456-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:865e58c6d0c5015ad76cd20e6c0cb1a2bf32a65d173e19a4eb7ad6fd0fca86bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4762079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16812069b8d64148a0225371e95b0533983a2557bc633a7a5b508c36e8bc0718`

```dockerfile
```

-	Layers:
	-	`sha256:992ecf1bac1f2e05b39148a595d48e2cdf3d36db294c2b7a5ec8ede6b8f5b779`  
		Last Modified: Tue, 23 Jul 2024 02:01:23 GMT  
		Size: 4.7 MB (4745870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a88acb85d86ed44b92f58b951697c016b59989f5548fa1185475621a2fe2e32`  
		Last Modified: Tue, 23 Jul 2024 02:01:22 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.11.3.1456-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:932c45527583bb76e0783aab8757c8b5e6ecb7b65d4922f0415061e69c8b0565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 MB (254641152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09547d2d2caad337375e81e969fd43f293c6dd046b0f12709e02f9bd8014a2a1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
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
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49207800cd3df526abfc01abd993093d7e4dc38ee68b7e14f2513db216d07dbc`  
		Last Modified: Tue, 02 Jul 2024 09:36:36 GMT  
		Size: 156.7 MB (156665628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e57e9be7d47082f5f01c1da502c9c3bc19609d2522cfe10e97372be494051c`  
		Last Modified: Tue, 02 Jul 2024 09:40:26 GMT  
		Size: 68.8 MB (68817920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661b23229b2fcbf0404e3a752363315e2a96e5e9bb0c5ccd7e520d5aed9e21bc`  
		Last Modified: Tue, 02 Jul 2024 09:40:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010eb359f8b1c111f4d7a4fe2c84317dba58234e703a5c447925cdbe56b37823`  
		Last Modified: Tue, 02 Jul 2024 09:40:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.11.3.1456-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:261516cffd4f807771f7432230663e86165477116273124fbb1c456dd60f39bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4728926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee33df8614f0b5effca66dbeec706fcd1f6b72901839a0b41b6eff94e14d78f`

```dockerfile
```

-	Layers:
	-	`sha256:42ea556b54cfdab0bf9d3bab9e3e24929603d55e72759d480cf56ef645fa217e`  
		Last Modified: Tue, 02 Jul 2024 09:40:24 GMT  
		Size: 4.7 MB (4712154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a00215760316e3c94361f7ce16f4df1dcccccf104a72d272ebcb51f9abc5a558`  
		Last Modified: Tue, 02 Jul 2024 09:40:24 GMT  
		Size: 16.8 KB (16772 bytes)  
		MIME: application/vnd.in-toto+json
