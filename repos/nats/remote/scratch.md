## `nats:scratch`

```console
$ docker pull nats@sha256:c81104c29f774ab6ac6178391029a857ca1b201750c9ebefad70bee0b9162cf6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:0b313c16824b8d98736c06153fa01af3c8d62eebc6298e9062fd2e00c0a3e865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a2333da61b6c9f0de1de8235aca52ee071283b0c8c6487d3ea15b4a0f9f8e2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:54120e60f5a574cbbfd83de2711330ae98499a27ff592bdb694994b87749dd23`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 6.3 MB (6282155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d71c31c70e45e814d8db85102321f1459be653c595cd91fafb76306cdf405e`  
		Last Modified: Mon, 31 Mar 2025 19:07:36 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b8d62bc797363d5eab76aea96ec144d02b901da4dba8eb8bf31cc4e51e3a09d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd51cd5b25ea5c4355cd2cde0e286d4f6da98802af9ed8b477001ff7ece4679`

```dockerfile
```

-	Layers:
	-	`sha256:19abc39a4cbb247bfa12363ce59bbce1e3bf861fddb9055c3a17e2d39d54d204`  
		Last Modified: Mon, 31 Mar 2025 19:07:36 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:af5758489c2981e0a1028dc47f82f0dd2d26e2fac7ac1e478a2a15a12029f6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6002169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17f13cf88d7cb6d029eafd34cd847cbacebb2131dc5b7ecfbed791e2958e6a4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:098bda892a4e7ddd77ca838f72ef9757e9b3cfae3c7bc97076a8dd0b6fd92597`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 6.0 MB (6001660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff1d2651842734b21329c25e1004a4da19102e57001381e60bb4fd58723fe19`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:736b8ee8472809de9731d9c426d2113e533e5ac68c9fbf4cd6bb44eb636b3d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffa52afcf9f827961f6f692daeb94f398721ac7559f559d56147558f6742150`

```dockerfile
```

-	Layers:
	-	`sha256:cc5887e8b88d73925b5364f9143ca37566f003a1560dffe173f7be8f10d66806`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:f1752b6d8b3a5506fab1fdf93ce66a6bd6e934d33a3c230231458f254ff505a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5992492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d3d700cbec0d68868397c08f331e9cee8a3e484035ab651de2414c1bc1039b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ae07ef7aadc186e26516a3b1a5bacd27b42c41b8d63efc540622587ef29be07`  
		Last Modified: Mon, 31 Mar 2025 17:41:36 GMT  
		Size: 6.0 MB (5991983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d132fb7bc19f6f368e535b5a46903e88d661e5c0f5e33c79b7d66b962039598`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:ff00ada993e928a0dbcd0e627e845b5f9c4d11042f0e089912b8ef2969c89876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab26b373d46f30d56fc9b9ecf02d3c518eb5ab041a8fbb69e562b49b1a864d9d`

```dockerfile
```

-	Layers:
	-	`sha256:d552b4d64ce37965149a8aaeed3a0eebd251066efc77cb63ad2307f9d0bbdef7`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 10.6 KB (10649 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a360fbbfeb6f19012e875675cf70ea15e5ea3d9e003d5ccf1a61adeed8d515c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad8d86003a865c09c995830bd52c9154c44e7976be35a0790b217a28445c6c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:813138f2f23c3f67c00cc3f899e890b4b46ad187b3c70730ab91bd63ff37fa6d`  
		Last Modified: Mon, 31 Mar 2025 17:41:30 GMT  
		Size: 5.8 MB (5776442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d132fb7bc19f6f368e535b5a46903e88d661e5c0f5e33c79b7d66b962039598`  
		Last Modified: Mon, 31 Mar 2025 20:44:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:13fe1989809a4185209660bba2e8a407b921e80a959889e94c8d6b18e6eadc66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebd7eb7627ea55d24e6c1b36e5124796e00e1a2243414d5b3f65ff44089ec66`

```dockerfile
```

-	Layers:
	-	`sha256:a33f391d8364f479953478aa1b1ce3f8e6e05c31407e5d9ead5d4d5db6da559f`  
		Last Modified: Mon, 31 Mar 2025 20:44:29 GMT  
		Size: 10.7 KB (10708 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:74e2df57ac704452ee531238216b3accd76025199ee310563732dd2c680227a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd71cf45edbcaea354422b03a686d602fac79be9357fdbc6b5c05d8ab8309e5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:452917a8c6e0add88a19efed21ff3bf850d722622f476c3b9d4426f3dbaaffb7`  
		Last Modified: Mon, 31 Mar 2025 17:41:27 GMT  
		Size: 5.8 MB (5756706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc09a85b63b7a6867f196c8c27905ad711a7457fa91d3df80022bc3d24111b3`  
		Last Modified: Mon, 31 Mar 2025 20:07:44 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9460476db24c3ccd45c6374ab5e0dfa8af2b95e6ed003b294fca69a3f6d49e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8048c19445dcae5f87494cedbc4822265fb6848963d3958920bc8a77dc19881`

```dockerfile
```

-	Layers:
	-	`sha256:2e79f43f61fe3cbbfb9fa2ab55acbd3a3254d4378c81f4bef4392b1b18e91f10`  
		Last Modified: Mon, 31 Mar 2025 20:07:44 GMT  
		Size: 10.6 KB (10613 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:6b9323c60c161cbd82daa5b02f46e55051f8540e7c9770dc1c2ed619086c6f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6122555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb48b95165c0163d0de0d793f09fa9aaa8dbc79c4b50241ee9e33ac819b1a501`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 31 Mar 2025 17:39:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 31 Mar 2025 17:39:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 31 Mar 2025 17:39:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 31 Mar 2025 17:39:54 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 31 Mar 2025 17:39:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cdb5d3b73d4e5760c377e2d1a31f668fd95251ac45157f6a4c4d98139b337e23`  
		Last Modified: Mon, 31 Mar 2025 17:41:31 GMT  
		Size: 6.1 MB (6122046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e9431fd0e418054b688573b0ef6c205ce09bcb9015c474b01a32d6800912d0`  
		Last Modified: Mon, 31 Mar 2025 20:07:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:2dfb1482f9d33c4a0f01a77e40b206f5b997b290b5e3899ee0c2678dd35731a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff58880fe981b8b31c473e8e992460d1ef7a218db9dd4ffc3a951750055bfd3`

```dockerfile
```

-	Layers:
	-	`sha256:9bb52fda18a732bf8f1ead6cd17dd200cfcae43fd84710a4ddb71372c0815f2b`  
		Last Modified: Mon, 31 Mar 2025 20:07:36 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json
