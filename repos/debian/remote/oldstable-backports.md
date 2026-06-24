## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:08bc9d40f40f1bfb96af57f60a62a5d9797af6037e97f66470c06a0bd35cdcdd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:5270c29f5b0cbb79b43542c490b479767f75dd9bdfefc97ecd4b0ba05f253922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48502270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897b5e4e2badf65bce685660c5a9ddfa9b5d572f4277fa84bf02070128c2bcbb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1781049600'
# Thu, 11 Jun 2026 00:15:58 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:9347f484150dbe9983a6bd278db05accfaead3a8dbfb600e0a4db46731c78140`  
		Last Modified: Wed, 10 Jun 2026 23:41:06 GMT  
		Size: 48.5 MB (48502046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b25289af95f91dd1426f833b35b2904291ae2a8ac4f34a4a3ce273ffa45634`  
		Last Modified: Thu, 11 Jun 2026 00:16:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4cb4f590eb6c46a4faa3a09c61d991309167eab6eac1ab5e4d87f7072057eb8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e03434dc4546db5646ae9e04918f61a1351b28b5619368b45084eca6e96521d`

```dockerfile
```

-	Layers:
	-	`sha256:d2044882aec473f39ddff24506346ae634fbaf8357601e44e97a5d286c4de081`  
		Last Modified: Thu, 11 Jun 2026 00:16:05 GMT  
		Size: 3.7 MB (3734112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85d82cd0b4d669bccd572466e8696e22ae2b4d0074fb3433e6d1a47ee27316ea`  
		Last Modified: Thu, 11 Jun 2026 00:16:04 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:4e1ea93b50064f9a762251e739ed7f54f1140a77bae8e90c5a92ae63243e0ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46038412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79dcb5785c9bcc3c9fb66c8e4c01e736f9a5c577e43b7f8b04cfc3cfca9f1e89`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'oldstable' '@1781049600'
# Thu, 11 Jun 2026 00:15:55 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d20f32b72a79ca7537e089f596bb93bd2af59e258b733e002eeb6f290736cedd`  
		Last Modified: Wed, 10 Jun 2026 23:38:44 GMT  
		Size: 46.0 MB (46038188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a108437b808fb9334f6e05c3a74b90de8f631681ad5b72f3ccd12d8c65f5d020`  
		Last Modified: Thu, 11 Jun 2026 00:16:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1323161382c5b9269054326cd6ec3d01d2879b5b9b2053b777deb9392b48668f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8776bc0ee3f57b3039b9a5d2e37302ad582d5a0dd2226031ed725a9fa6cd1caf`

```dockerfile
```

-	Layers:
	-	`sha256:75de918a12bc740b96bce82ff9b9cc35ddaab3b3142b74e31e0d32aa3df11613`  
		Last Modified: Thu, 11 Jun 2026 00:16:02 GMT  
		Size: 3.7 MB (3734313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50298948f919b6be5db8b717ce22b3a79d7a6ce90c145be72b8e20f793506986`  
		Last Modified: Thu, 11 Jun 2026 00:16:01 GMT  
		Size: 5.9 KB (5866 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:07f2b235d64ae12b7a27e5f7caffa8c138efc64451e27720ed5568723333d860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44208294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3907c6179ebc668e18ff203a66236ce48a3ed7e608bcb55f152ccc8a171a22`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1781049600'
# Thu, 11 Jun 2026 00:15:13 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2b9657dbecb6b81567b11fccd5c44ea0616abfb91e7d77a9d0b86e0713b75c8f`  
		Last Modified: Wed, 10 Jun 2026 23:42:28 GMT  
		Size: 44.2 MB (44208069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06a9c18ff78e1b838fea6a41e2f304513f0666e5d207d3451058c8949b6d48f`  
		Last Modified: Thu, 11 Jun 2026 00:15:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:50a8ba7953f503d2011d214a326ea022a5b1fc359a2480b6ae5a749e97509239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3742157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7ae2c4b3e85e1efdd3ef28a8cd1fa99d80d7885b256e812a6d3018d014e190`

```dockerfile
```

-	Layers:
	-	`sha256:7f4058d5eba88f24c00cf48b414e0b48facd148b17729be1ebb25dc644e3c47d`  
		Last Modified: Thu, 11 Jun 2026 00:15:19 GMT  
		Size: 3.7 MB (3736291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:065bbda002fffa732a5be6ad4b6331831d3b2acc0d45669e4f1465212683e863`  
		Last Modified: Thu, 11 Jun 2026 00:15:19 GMT  
		Size: 5.9 KB (5866 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:fa6ce5d1b71332c2ab94ddcff6157e5fd69fa24a5b5458f5eac76842ee721518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48389242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00656639147e3330b45ac14cbd3ad342949eedccfeae7ee770ac865cf37546d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1781049600'
# Thu, 11 Jun 2026 00:15:35 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:235e533a58c20e6b7b493f127e93c241fbaf901f4b0b284c17c677b6d10efe2c`  
		Last Modified: Wed, 10 Jun 2026 23:39:45 GMT  
		Size: 48.4 MB (48389019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d38fe9bb7357be7df699cb56ed9315a9c4197135cb0b8ac4263d7574c9553fb`  
		Last Modified: Thu, 11 Jun 2026 00:15:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:11fcf180843674e006fa2d3f172b698f781c0f385c04ed2d8f66b7e8d87f6ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf6599e6e23fec52c9067b1f6636006bceddef9f8c2e9387c974b42c192dccf`

```dockerfile
```

-	Layers:
	-	`sha256:5ab86e3603b64249a01434f3a4dcd547e926ed55f17ea0e762ae93a90a17b340`  
		Last Modified: Thu, 11 Jun 2026 00:15:42 GMT  
		Size: 3.7 MB (3734327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48ac08b913b3d0038a2ddc59fdc9d17042c1d98ddd96bde88243efc933b8af97`  
		Last Modified: Thu, 11 Jun 2026 00:15:42 GMT  
		Size: 5.9 KB (5878 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:7bc03bdb4832b9ee4da9cafd7fc39eea6908f77c2e30d273e5f6ba2ba4215eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49491603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d4f4c8f39f8b2efe674b98b24ca14066a618bc9128c91b1afae7730893079a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1782172800'
# Wed, 24 Jun 2026 01:15:11 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e6213bcdf45cd66db90d443212473e95a3ebaf64323e5130e2f5276ce9ae3072`  
		Last Modified: Wed, 24 Jun 2026 00:28:51 GMT  
		Size: 49.5 MB (49491379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421744dd4338f64087310f27bb7bf618501a0da265f954100bbb10ae8f7e2cd5`  
		Last Modified: Wed, 24 Jun 2026 01:15:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:bde320dcc46c3ce2ec6faa42accb97234637d6f1f7c55a6e5ec258ccb134a5b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7945d92b96cbd60e207e7aa36cc1156ac9283c03c78241e31aa8c7c114da1632`

```dockerfile
```

-	Layers:
	-	`sha256:a4337d906dc3387bc9def2e3b5064ffd6a9034430d6a7679af24f911f0aeb79d`  
		Last Modified: Wed, 24 Jun 2026 01:15:19 GMT  
		Size: 3.7 MB (3731308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:403f2f4f23c79d286c62f57b065cfcbad2a575f046914c60eb60905415aa4317`  
		Last Modified: Wed, 24 Jun 2026 01:15:19 GMT  
		Size: 5.8 KB (5792 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:14ebc16075d6feb5c292466062bb013a54cf8a8ea3b995fa1f7c6d8e600537b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48793052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6345906d6012c28bfcb18cda7b957257bd5ef7105cc43b3b41a03faa79a392e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'oldstable' '@1782172800'
# Wed, 24 Jun 2026 01:16:01 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c0f8845a6ed633a3c4e2a8e73bcdec5453e3a375f32e6fb2ee6863c8530a0bc4`  
		Last Modified: Wed, 24 Jun 2026 00:28:06 GMT  
		Size: 48.8 MB (48792827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e831fab755e1be19a5547d051214de049d50c93b7637cfa74e5eb2f3996d8b53`  
		Last Modified: Wed, 24 Jun 2026 01:16:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4b6d859cdcf08112f926a1128554d223bb2f6cd065e82cfdcf1df78b5c222430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fedff23176b87d674f27b73e66c0fc8c000053ec4799916913d88239ca90fd5a`

```dockerfile
```

-	Layers:
	-	`sha256:9c5058ff984ab0a255564ce48377b60edbddff6d350d4c24fc075a81fd9ac678`  
		Last Modified: Wed, 24 Jun 2026 01:16:19 GMT  
		Size: 5.6 KB (5634 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:4a508527016f248568d425de32b018914e7208dca4217a5777459c71005e5d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52347069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ba99624814e8fb301f31cc36761d4ef6e1851c7653503f7c73bd90081a7a63`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'oldstable' '@1782172800'
# Wed, 24 Jun 2026 01:14:16 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7321cb28d57d6b7c8ccdac8d30ebcefbda3f442b22ab533a0b2aef2f6f28fae3`  
		Last Modified: Wed, 24 Jun 2026 00:28:32 GMT  
		Size: 52.3 MB (52346845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605def5d6d6333b067ef56f70f51c6c1fe5f8226d714a22d6c8d371a0cf2ba6f`  
		Last Modified: Wed, 24 Jun 2026 01:14:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1022a990184a92ab733483573a3ef229b00104b9fad096dae569fcb30efec652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df970a1b15456cac36bce76ca49591d6678c55f1f31e26583b4158039491e3ee`

```dockerfile
```

-	Layers:
	-	`sha256:cde68b85f459c639898db8d0e6bb612ae382aa5f66fe0c6f2329564c55e51820`  
		Last Modified: Wed, 24 Jun 2026 01:14:32 GMT  
		Size: 3.7 MB (3738470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5dddc45c8b0ee56115258056a5b0d42dd33f47f3b958175a35bdde155692161`  
		Last Modified: Wed, 24 Jun 2026 01:14:31 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:e6dbc6bbbe9e0525a9c1e6fe082e21900e8535b59d64a5bc5cacb9152711a8ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47161905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e123168174f802d98f310bf0ffe8324b31489e5f1a712a74d645d46a100aa652`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'oldstable' '@1782172800'
# Wed, 24 Jun 2026 01:14:07 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0f945b9568267786adbceb79f99464d6fe2a758310e284cb0ce77072f0fe24a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:40 GMT  
		Size: 47.2 MB (47161680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2ccb1544199ba755f0ddb0986e43def44de4877614702ecdf1ab7ce7ec8161`  
		Last Modified: Wed, 24 Jun 2026 01:14:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:80c746be48912dac965b585adf9c7ff323719e62c94a4e5658c6aab5803adc4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66a5b1dae3e51a0d9b6b81b766f31f0064070a3426fa8634f0631cff7c0d307`

```dockerfile
```

-	Layers:
	-	`sha256:fd30c774eb42c49a7cb4a96c73d2dfa36b58d7e6e360f4d8911b955038ae6592`  
		Last Modified: Wed, 24 Jun 2026 01:14:18 GMT  
		Size: 3.7 MB (3730950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e190182a984a52a317f6c14e8ac00b7001b1dc9fb4faa5eb2ba56e81be4bc7`  
		Last Modified: Wed, 24 Jun 2026 01:14:18 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json
