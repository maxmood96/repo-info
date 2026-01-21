## `sapmachine:21-jre-alpine-3.21`

```console
$ docker pull sapmachine@sha256:3dad6459f5fdbb06966c36553ae6480dd6ddee70e50863f30e2267c42fd2c6dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:21-jre-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:7597d5d497e84ba6675b8fec33d1779ec9bd36225fe501ee4d43dc1d6e8f33b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63787566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e2d09e2877637d94866a2d537265bc2aa0dbde1df638b85da6f5b2f64cbaef`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 21:30:29 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-21-jre=21.0.9-r0 # buildkit
# Tue, 21 Oct 2025 21:30:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-sapmachine-jre
# Tue, 21 Oct 2025 21:30:29 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4b64f9d7a7e10f7bb6af11840c8ba26f4d87978baaa8bc3217034d4734ae2b`  
		Last Modified: Wed, 22 Oct 2025 02:43:27 GMT  
		Size: 60.1 MB (60144997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9de8dc29462dc9f1a2e60cf89b1148b96822f96fcc6c4f4d028bd2dffb8b4d38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.7 KB (430709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55383dc4073aa12f8547213f9916f3d25e8e5afe6eb3f44cded0ad006c195d5`

```dockerfile
```

-	Layers:
	-	`sha256:279e853f4c7142f5e96c4d7c6eac028a9b65c9defaa2a2af76a102bb26953710`  
		Last Modified: Wed, 22 Oct 2025 02:43:26 GMT  
		Size: 423.7 KB (423710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c88df8ab98abf238ad52d6ce2c4e07aed63418cb35a8a603d97ff0ad5ef4dfed`  
		Last Modified: Wed, 22 Oct 2025 02:43:26 GMT  
		Size: 7.0 KB (6999 bytes)  
		MIME: application/vnd.in-toto+json
