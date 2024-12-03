## `gazebo:libgazebo11`

```console
$ docker pull gazebo@sha256:f515a05d208c51bd01f4e5ff5edddbf7184e1518b11956ec0e1ddd8ef37c0d26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gazebo:libgazebo11` - linux; amd64

```console
$ docker pull gazebo@sha256:1ed9219bfa06a16aef8d63207329259c137ea7c02798865250876fc298029b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.0 MB (609016991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7475336507cdfa1d0e3034c0eedbe64325b392c41a503de3c235a85ec883c626`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Thu, 28 Nov 2024 06:47:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Nov 2024 06:47:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Nov 2024 06:47:41 GMT
RUN set -eux; 	key='D2486D2DD83DB69272AFE98867170598AF249743'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /usr/share/keyrings; 	gpg --batch --export "$key" > /usr/share/keyrings/pkgs-osrf-archive-keyring.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 28 Nov 2024 06:47:41 GMT
RUN . /etc/os-release     && echo "deb [ signed-by=/usr/share/keyrings/pkgs-osrf-archive-keyring.gpg ] http://packages.osrfoundation.org/gazebo/$ID-stable $VERSION_CODENAME main" > /etc/apt/sources.list.d/gazebo-latest.list # buildkit
# Thu, 28 Nov 2024 06:47:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.15.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Nov 2024 06:47:41 GMT
EXPOSE map[11345/tcp:{}]
# Thu, 28 Nov 2024 06:47:41 GMT
COPY ./gzserver_entrypoint.sh / # buildkit
# Thu, 28 Nov 2024 06:47:41 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 28 Nov 2024 06:47:41 GMT
CMD ["gzserver"]
# Thu, 28 Nov 2024 06:47:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.15.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83071177be7c7bec24605107bc20da1f92ff5f8bd8c6c60dbeba2b1234591ef`  
		Last Modified: Mon, 02 Dec 2024 20:29:57 GMT  
		Size: 1.2 MB (1198850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93494aa21f34334db98ac2d6df6d925cb32bdd139017cf7997e858a04d37578e`  
		Last Modified: Mon, 02 Dec 2024 20:29:57 GMT  
		Size: 5.4 MB (5361848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f7c7f683b3d144e6f8edafc518b2372e9bb39ac75d623f7ced6ff5a87db5ea`  
		Last Modified: Mon, 02 Dec 2024 20:29:57 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8e82a107c13d8eb46fba7a043eadd0907b13adffec5ac4bf878a60176e6edd`  
		Last Modified: Mon, 02 Dec 2024 20:29:57 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7baa10ae3e83af0aaa184f8fafdf2eac039b23d12c34c2ac3e511e2a47123b`  
		Last Modified: Mon, 02 Dec 2024 20:30:02 GMT  
		Size: 278.0 MB (277997659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4b18484b8d994d54e0867bac33f684b86cf01a8edf6e0620c5a3aead32647d`  
		Last Modified: Mon, 02 Dec 2024 20:29:58 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9a4ea8694c031b6529ca9947ee7f5f6a3d673f45ead5d585beb1b7fb7fa5a6`  
		Last Modified: Mon, 02 Dec 2024 21:09:51 GMT  
		Size: 296.9 MB (296945641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gazebo:libgazebo11` - unknown; unknown

```console
$ docker pull gazebo@sha256:fb2f666c221d578a8331543b8b70907e872577b8638f48d0c3fdc1a3162b22ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37550375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551b3c6ce980c59ab6cda1bdb21324174acc1970f732a1a1a3a964df8032cd04`

```dockerfile
```

-	Layers:
	-	`sha256:8a78df4aac01bb814b75f5341acdb55da308db837681b1f2bbc24e73a13987af`  
		Last Modified: Mon, 02 Dec 2024 21:09:46 GMT  
		Size: 37.5 MB (37541712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1be51d1868b6c8a495f09d9e2b3c4ddc435631fff59d5fb419cbce116d836d1a`  
		Last Modified: Mon, 02 Dec 2024 21:09:46 GMT  
		Size: 8.7 KB (8663 bytes)  
		MIME: application/vnd.in-toto+json
