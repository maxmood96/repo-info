## `debian:testing-backports`

```console
$ docker pull debian@sha256:df934889f2541af32530b3af6e8aafc1258de83ac8a8f0bc82eafb0b5a978f4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:9b09e79e2c089bb838845fa2d90eaded5458f152e8b4262359ce1e222fd1e04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48677403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ae2a70d15002c3bceb0c1353cc137ff7380eb671acbc4ff2b67a6e63224ca6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1771804800'
# Tue, 24 Feb 2026 18:52:02 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:34be0fb38bdb10b6efea64895d8af767ee0135f3467c8cbf6b2a7ad809ff66f7`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 48.7 MB (48677181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd0a8a152a214d1e54f2d3ea0112e0b5e903ca3d3b0da6f3b9b41b3fb760e66`  
		Last Modified: Tue, 24 Feb 2026 18:52:08 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2f0a9c19ae42b4040e37695d21af14e494e9dab7e39864fc1c7213804e93d7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3153358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91481188bf57c1f0aa158f60f5f87a4c1c271bed2a9842130faebc1d7813481`

```dockerfile
```

-	Layers:
	-	`sha256:dcc0f3cf446c732be6cb85a4801204eb08985e7b7e7368a6f490bd4cf6e217f4`  
		Last Modified: Tue, 24 Feb 2026 18:52:09 GMT  
		Size: 3.1 MB (3147564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aad2f264c7357996b12f48b13d4ac6f98683aa7b6ac9d2ea630143864d79245f`  
		Last Modified: Tue, 24 Feb 2026 18:52:08 GMT  
		Size: 5.8 KB (5794 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:5203418f9bfd655f347f126e2df0b775eff6095af88a30123fc98c0bba0d9f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45653270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fdb33030f62e47b850ed7cff47a7fe89e1d24932681e0f981d5dc990391a65d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'testing' '@1771804800'
# Tue, 24 Feb 2026 18:57:15 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1c630a6e27c3fdfd1daa4bb58f15468fbbec7c8831146742a1e3361221a95f72`  
		Last Modified: Tue, 24 Feb 2026 18:42:42 GMT  
		Size: 45.7 MB (45653048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ccc5965dc5853c6d5f3a78c88bd29f04f1691239079f1dd4cf605b5b3e663f`  
		Last Modified: Tue, 24 Feb 2026 18:57:22 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6afff8735387b7c9e9f7dc923130598b663eea1b60d0f37e0bd707fbab172510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e114868e7691cbd66f7cb61fafa2684ad6a5dfabe10ef1b906672e2c22ade8b`

```dockerfile
```

-	Layers:
	-	`sha256:eb57ca19c055291a79132df9dcef372643705d9dc816c8529085bda94b53d67d`  
		Last Modified: Tue, 24 Feb 2026 18:57:22 GMT  
		Size: 3.1 MB (3148932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9234e8421364a14db2b149e54fe040dd451e337cce8bfdc4a755c58ad28769f2`  
		Last Modified: Tue, 24 Feb 2026 18:57:21 GMT  
		Size: 5.8 KB (5850 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:4d931661e8e31e83c1522a636ac21c6ca81fe77bd4ac1d3c107373f434150992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48705248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd95b17e3a0ad7468b9564d506523d3f2cdb8c2b64ba0ae182322ada7ec4d3a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1771804800'
# Tue, 24 Feb 2026 18:57:06 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c8a993150206adc8ed6d5444bc6073fe1f1f2401037e10aa375ccb6fbef8932e`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 48.7 MB (48705026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8599e5be3faea176c92c44ec1632adef5eac9fb1ea60f8a8b78974ab0bc832eb`  
		Last Modified: Tue, 24 Feb 2026 18:57:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:18e430700e8bb048736196d16c112036036c0941d08ecce2d7e7db325a98fe67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba14eb8baba14063ec7e0d37b622df502f902f954048c8eac8260903209a9d77`

```dockerfile
```

-	Layers:
	-	`sha256:b0dc27f36be5ee64309d09f647b7b5a4bdacf77c47c4537294198756314b5469`  
		Last Modified: Tue, 24 Feb 2026 18:57:12 GMT  
		Size: 3.2 MB (3155612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e4e8a53267f1964f7e66407664af50b47b894dd6f911042864b00b4e0cfde4d`  
		Last Modified: Tue, 24 Feb 2026 18:57:12 GMT  
		Size: 5.9 KB (5861 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:31d8a5373cbe9aec6fab41e45f0d6ddb3396c3dd56c18833f1db8dc7daec40b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50012191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a493c842189b86f7747d2b78a66c8f3db1fc5aa16aab3607e4544539f8bc2fa7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'testing' '@1771804800'
# Tue, 24 Feb 2026 18:53:55 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f9081786ac0967d3cbd44437a7200aaad92b27a3e16ff6455f754428b73fd8d7`  
		Last Modified: Tue, 24 Feb 2026 18:42:34 GMT  
		Size: 50.0 MB (50011968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df333d1a9ee437a7e8ffcbfc86fbb9e46dd8e61f4e6530ec0e11e552471c4ab`  
		Last Modified: Tue, 24 Feb 2026 18:54:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2818aaef03586410723112489caae4cfde0a1caf29b1a60181fb7816c27a6ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3150538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8498a6bd26248e64db0567bda4d4dbbd19ccfc4a3c1a64596f3f575b027be14`

```dockerfile
```

-	Layers:
	-	`sha256:f65aedd06885c4c319a9c0e3cd49abd40985cef96aa9d351864459845b6d5a2e`  
		Last Modified: Tue, 24 Feb 2026 18:54:02 GMT  
		Size: 3.1 MB (3144762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56e843e29b6a8320a9109e8bc58a24348698c2a92adc84d9702dbd0450e1a384`  
		Last Modified: Tue, 24 Feb 2026 18:54:01 GMT  
		Size: 5.8 KB (5776 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:ea377890dcfcb16f0dbfd1aaa54a9034225872a7c85ed64c981e23b13cf8d661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53642008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5afa48122ea14517353bce77f3ab8b8c7d1ec88d544a43bb47200cabf67e42`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1771804800'
# Tue, 24 Feb 2026 18:54:39 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a9c7d7625b810d130976f4d65172bc2e59635199240180b43a17644df8a7c067`  
		Last Modified: Tue, 24 Feb 2026 18:44:39 GMT  
		Size: 53.6 MB (53641787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed84671a97ceb4d69bade2803d1ef8bc3fd7d496ad22ae9b6b40ae4f9d2ccb73`  
		Last Modified: Tue, 24 Feb 2026 18:54:54 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9902febbab3cd27e9e44dd510870d150aaf125e79680f08cdff08c37b1321d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e75018cfd2885acb7413496918a60c6f330df44b979e0da98101e646c443708`

```dockerfile
```

-	Layers:
	-	`sha256:6106d6752cdacf41394aa840a6831cbb7804c3eb4cf6536e1a2b2ba6256c31e9`  
		Last Modified: Tue, 24 Feb 2026 18:54:54 GMT  
		Size: 3.2 MB (3151079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bb56fbfe1370a67ba5926aa938840b3cfc297ce3f67472dd7d6f7254455e0b9`  
		Last Modified: Tue, 24 Feb 2026 18:54:54 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:7f491d2d10bf79f4963f0e6982bcb7512ec0188438c838b391bf9ebe31190f01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46895415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4447f3cdb3e03670716843182850c5e28c2a7ec7b60a12c4aa2417ebf1441953`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'testing' '@1769990400'
# Tue, 03 Feb 2026 09:02:34 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c1c84fde2ddca8f6d2a89a1fc0e373bb708dada789d8014cd228e300a857f5b4`  
		Last Modified: Tue, 03 Feb 2026 07:09:22 GMT  
		Size: 46.9 MB (46895195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84884172907ba1bed6795c0da775781280b48260921b93ded0e2dd95f8c2f0e`  
		Last Modified: Tue, 03 Feb 2026 09:03:29 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8946ab71abec7df5b9f432171c06127c6f67efe68399af2296941728e3f68652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3148299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a20585a483d94422bf1182fcb8ac8a52455574f8da79a75fc5e4cb49f7a503`

```dockerfile
```

-	Layers:
	-	`sha256:4b9dbd0ac64468ceed85b227ee122b7adcc21139352a2810b9bfeacd228652ab`  
		Last Modified: Tue, 03 Feb 2026 09:03:29 GMT  
		Size: 3.1 MB (3142479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17bfcc187c2a9b56ba7b60622aad780195e79c80d0aaebb6f45d44742291fd54`  
		Last Modified: Tue, 03 Feb 2026 09:03:29 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:f9191bf4bf01dae7ceac2af4f2d8e2269a31af56cc9316b1ef16dbd03730aed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48448575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9229852ba47adbdcbdb1e2e06fb0a766d9f2d15fb8100a1f2e8e6fac2b37b0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1771804800'
# Tue, 24 Feb 2026 18:54:02 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:fc75b039b41eab51d245e601a0ca918f28836808b7ae484f3d0e33c4db6b6ceb`  
		Last Modified: Tue, 24 Feb 2026 18:43:05 GMT  
		Size: 48.4 MB (48448352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481cc9b8a5805a33395f6cd788ab917bc18399bbc3720d13e83b1bb411b34e77`  
		Last Modified: Tue, 24 Feb 2026 18:54:18 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a184d39c3a98d63ca901e5491f81fb6e30c8f9c7c46640d5351207178d57ff53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e224154cd756ed0c7a73dea3751432b1ae2302e01252b214012a3e4bbf6a711a`

```dockerfile
```

-	Layers:
	-	`sha256:9d1c38301db0ee8b9daaf217dcf7cedd98b22a5acf000b743730e7dd63f3e0d8`  
		Last Modified: Tue, 24 Feb 2026 18:54:18 GMT  
		Size: 3.1 MB (3149013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bae6d3f95728d61b8bdb93e05b7b4148dd1ddf6badcc56eaf7da1341361e6c87`  
		Last Modified: Tue, 24 Feb 2026 18:54:18 GMT  
		Size: 5.8 KB (5794 bytes)  
		MIME: application/vnd.in-toto+json
