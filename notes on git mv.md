```
689  git co experiment/RUN-1185-isolate-pending-cancel-recreated-from-master
696  git co -b experiment/RUN-1185-pending-cancel-moved
697  cd packages/sp-pending-cancel/
699  cd src/
701  cd pages/
703  git rm -rf ./choose-pack/
704  git rm -rf ./retentions-*
705  git rm -rf shared/retentions
706  git st
707  git add .
708  git commit -m 'chore(pending-cancel): project removed'
709  git st
710  git mv ../../../sp-shop-select-journey/src/pages/choose-pack ./
711  git mv ../../../sp-shop-select-journey/src/pages/retentions-* ./
712  git mv ../../../sp-shop-select-journey/src/pages/shared/retentions ./shared/
718  git add .
719  git commit -m 'chore(pending-cancel): moved project to pending-cancel'
721  git co -b pending-cancel/RUN-948-top-tier-v2
722  git merge feature/RUN-948-top-tier-v2
```
GIT OUTPUT:
```
Auto-merging packages/sp-pending-cancel/src/pages/shared/retentions/utils/basket-references.spec.js
Auto-merging packages/sp-pending-cancel/src/pages/shared/retentions/utils/basket-references.js
Auto-merging packages/sp-pending-cancel/src/pages/shared/retentions/selectors/product-content.spec.js
Auto-merging packages/sp-pending-cancel/src/pages/shared/retentions/selectors/product-content.js
Auto-merging packages/sp-pending-cancel/src/pages/shared/retentions/fixtures/propositions.js
Auto-merging packages/sp-pending-cancel/src/pages/shared/retentions/fixtures/products.js
Auto-merging packages/sp-pending-cancel/src/pages/shared/retentions/fixtures/mock-gql-response-simpleBasket.js
Auto-merging packages/sp-pending-cancel/src/pages/shared/retentions/data/retentions-proposition-offers/shallow-offer.js
Auto-merging packages/sp-pending-cancel/src/pages/shared/retentions/data/retentions-proposition-offers/shallow-offer-variety.js
Auto-merging packages/sp-pending-cancel/src/pages/shared/retentions/data/retentions-proposition-offers/shallow-offer-original.js
Auto-merging packages/sp-pending-cancel/src/pages/shared/retentions/data/retentions-proposition-offers/shallow-offer-box-sets.js
Auto-merging packages/sp-pending-cancel/src/pages/shared/retentions/data/retentions-proposition-offers/medium-offer.js
Auto-merging packages/sp-pending-cancel/src/pages/shared/retentions/data/retentions-proposition-offers/medium-offer-variety.js
Auto-merging packages/sp-pending-cancel/src/pages/shared/retentions/data/retentions-proposition-offers/medium-offer-original.js
Auto-merging packages/sp-pending-cancel/src/pages/shared/retentions/data/retentions-proposition-offers/medium-offer-box-sets.js
Auto-merging packages/sp-pending-cancel/src/pages/shared/retentions/data/retentions-proposition-offers/deep-offer.js
Auto-merging packages/sp-pending-cancel/src/pages/shared/retentions/data/retentions-proposition-offers/deep-offer-variety.js
Auto-merging packages/sp-pending-cancel/src/pages/shared/retentions/data/retentions-proposition-offers/deep-offer-original.js
Auto-merging packages/sp-pending-cancel/src/pages/shared/retentions/data/retentions-proposition-offers/deep-offer-box-sets.js
Auto-merging packages/sp-pending-cancel/src/pages/shared/retentions/constants/index.js
Auto-merging packages/sp-pending-cancel/src/pages/retentions-confirmation/selectors/retentions-confirmation.js
Auto-merging packages/sp-pending-cancel/src/pages/retentions-confirmation/fixtures/basket-state.js
Auto-merging packages/sp-pending-cancel/src/pages/choose-pack/selectors/choose-pack-selector.spec.js
Auto-merging packages/sp-pending-cancel/src/pages/choose-pack/selectors/basket-selector.spec.js
Auto-merging packages/sp-pending-cancel/src/pages/choose-pack/actions/remove-retentions-basket-item.spec.js
Auto-merging packages/sp-pending-cancel/src/pages/choose-pack/actions/remove-retentions-basket-item.js
Auto-merging packages/sp-pending-cancel/src/pages/choose-pack/actions/fetch-proposition-and-basket.spec.js
Auto-merging packages/sp-pending-cancel/src/pages/choose-pack/actions/add-retentions-basket-item.spec.js
Auto-merging packages/sp-pending-cancel/src/pages/choose-pack/actions/add-retentions-basket-item.js
Merge made by the 'recursive' strategy.
 packages/sp-pending-cancel/src/pages/choose-pack/actions/add-retentions-basket-item.js                                   |   6 ++-
 packages/sp-pending-cancel/src/pages/choose-pack/actions/add-retentions-basket-item.spec.js                              | 188 +++++++++++++++++++++++++++++++++++++++++++----------------------
 packages/sp-pending-cancel/src/pages/choose-pack/actions/fetch-proposition-and-basket.spec.js                            |  50 ++++++++++++++----
 packages/sp-pending-cancel/src/pages/choose-pack/actions/remove-retentions-basket-item.js                                |  14 +++--
 packages/sp-pending-cancel/src/pages/choose-pack/actions/remove-retentions-basket-item.spec.js                           | 220 ++++++++++++++++++++++++++++++++++++++++++++++++++++++-----------------------
 packages/sp-pending-cancel/src/pages/choose-pack/selectors/basket-selector.spec.js                                       |  68 +++++++++++++++---------
 packages/sp-pending-cancel/src/pages/choose-pack/selectors/choose-pack-selector.spec.js                                  |  24 +++++++++
 packages/sp-pending-cancel/src/pages/retentions-confirmation/fixtures/basket-state.js                                    |   6 +--
 packages/sp-pending-cancel/src/pages/retentions-confirmation/selectors/retentions-confirmation.js                        |  12 ++++-
 packages/sp-pending-cancel/src/pages/shared/retentions/constants/index.js                                                |   2 +
 packages/sp-pending-cancel/src/pages/shared/retentions/data/retentions-proposition-offers/deep-offer-box-sets.js         |   9 +++-
 packages/sp-pending-cancel/src/pages/shared/retentions/data/retentions-proposition-offers/deep-offer-original.js         |   9 +++-
 packages/sp-pending-cancel/src/pages/shared/retentions/data/retentions-proposition-offers/deep-offer-variety.js          |   9 +++-
 packages/sp-pending-cancel/src/pages/shared/retentions/data/retentions-proposition-offers/deep-offer.js                  |   9 +++-
 packages/sp-pending-cancel/src/pages/shared/retentions/data/retentions-proposition-offers/medium-offer-box-sets.js       |   9 +++-
 packages/sp-pending-cancel/src/pages/shared/retentions/data/retentions-proposition-offers/medium-offer-original.js       |  10 +++-
 packages/sp-pending-cancel/src/pages/shared/retentions/data/retentions-proposition-offers/medium-offer-variety.js        |   9 +++-
 packages/sp-pending-cancel/src/pages/shared/retentions/data/retentions-proposition-offers/medium-offer.js                |   9 +++-
 packages/sp-pending-cancel/src/pages/shared/retentions/data/retentions-proposition-offers/shallow-offer-box-sets.js      |   9 +++-
 packages/sp-pending-cancel/src/pages/shared/retentions/data/retentions-proposition-offers/shallow-offer-original.js      |   9 +++-
 packages/sp-pending-cancel/src/pages/shared/retentions/data/retentions-proposition-offers/shallow-offer-variety.js       |   9 +++-
 packages/sp-pending-cancel/src/pages/shared/retentions/data/retentions-proposition-offers/shallow-offer.js               |   9 +++-
 packages/sp-pending-cancel/src/pages/shared/retentions/fixtures/mock-gql-response-simpleBasket.js                        |   7 +++
 packages/sp-pending-cancel/src/pages/shared/retentions/fixtures/products.js                                              |  20 ++++---
 packages/sp-pending-cancel/src/pages/shared/retentions/fixtures/propositions.js                                          |  29 ++++++++---
 packages/sp-pending-cancel/src/pages/shared/retentions/selectors/product-content.js                                      |  27 +++++++---
 packages/sp-pending-cancel/src/pages/shared/retentions/selectors/product-content.spec.js                                 |  51 +++++++++++++++---
 packages/sp-pending-cancel/src/pages/shared/retentions/utils/basket-references.js                                        |  10 ++--
 packages/sp-pending-cancel/src/pages/shared/retentions/utils/basket-references.spec.js                                   |  30 +++++++++--
 packages/sp-shop-select-journey/src/constants/retentions-pending-cancel.js                                               |   1 +
 packages/sp-shop-select-journey/src/pages/shared/retentions/data/retentions-proposition-offers/static-type-check.spec.js |  25 +++++++++
 packages/sp-shop-select-journey/src/pages/shared/retentions/data/top-tier-fake-content.js                                |  67 ++++++++++++++++++++++++
 packages/sp-shop-select-journey/src/pages/shared/retentions/utils/basket-top-tier.js                                     |  31 +++++++++++
 packages/sp-shop-select-journey/src/pages/shared/retentions/utils/basket-top-tier.spec.js                                | 104 ++++++++++++++++++++++++++++++++++++
 34 files changed, 881 insertions(+), 220 deletions(-)
 create mode 100644 packages/sp-shop-select-journey/src/pages/shared/retentions/data/retentions-proposition-offers/static-type-check.spec.js
 create mode 100644 packages/sp-shop-select-journey/src/pages/shared/retentions/data/top-tier-fake-content.js
 create mode 100644 packages/sp-shop-select-journey/src/pages/shared/retentions/utils/basket-top-tier.js
 create mode 100644 packages/sp-shop-select-journey/src/pages/shared/retentions/utils/basket-top-tier.spec.js
 ```

As you can see everything works **EXCEPT**:
- `packages/sp-shop-select-journey/src/constants/retentions-pending-cancel.js` Which should be explicitly moved before-hand. Probabliy we will need to check other files that are totally ours in weird locations, like the routes configurations and others.
- the `create` operations, these could been save by using the following:

### Get all the created files and add a last commit moving them to the proper place.
git mv ./packages/sp-shop-select-journey/src/pages/shared/retentions/data/retentions-proposition-offers/static-type-check.spec.js ./packages/sp-pending-cancel/src/pages/shared/retentions/data/retentions-proposition-offers/static-type-check.spec.js
git mv ./packages/sp-shop-select-journey/src/pages/shared/retentions/data/top-tier-fake-content.js ./packages/sp-pending-cancel/src/pages/shared/retentions/data/top-tier-fake-content.js
git mv ./packages/sp-shop-select-journey/src/pages/shared/retentions/utils/basket-top-tier.js ./packages/sp-pending-cancel/src/pages/shared/retentions/utils/basket-top-tier.js
git mv ./packages/sp-shop-select-journey/src/pages/shared/retentions/utils/basket-top-tier.spec.js ./packages/sp-pending-cancel/src/pages/shared/retentions/utils/basket-top-tier.spec.js

### Or create a patch of all the changes done in a branch with all the paths already fixed
`git diff ${BASE}...${BRANCH} | sed -e 's/b\/packages\/sp-shop-select-journey/b\/packages\/sp-pending-cancel/'`

The only problem with this is that will we have squashed the changes after it.
We could write a script that generates a patch for each commit introduced in a branch and recreate them (with broken time stamps) but at least we could keep the "changelog" if necessary

git mv ./packages/sp-shop-select-journey/src/pages/shared/retentions ./packages/sp-pending-cancel/src/pages/shared

## POST STEPS
Probably at the end of each branch to be recreated like this, we will need to re add the **original files** that were Moved to sp-pending-cancel from sp-shop-select-journey so that sp-shop-select-journey will not be actually altered, as with those files removed, the compilation and execution of sp-shop-select-journey will fail.
This could cause problems merging story by story to master, so maybe we should do a massive merge with all what we have together.

Something like this:
- Merge `experiment/RUN-1185-isolate-pending-cancel-recreated-from-master` to `master`
- Create of  `experiment/RUN-1185-RUN-1185-pending-cancel-moved` (moves all our stuff from sp-shop-select-journey to sp-pending-cancel)
- Merge upon it all the unmerged cards using the technique describe above (merge, mv created files)
- Copy **original files** of pending-cancel into sp-shop-select-journey (so no alteration compared with master)
- Merge it to master
- Be happy :D
