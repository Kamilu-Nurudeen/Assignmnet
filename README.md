# Assignmnet

function assignment(sentence) {
//   assumptions sentence cannot have less than 2 words
  const wordList = sentence.split(" ")
  if (wordList.length < 2) {
    return "Sentence must have 2 or more words"
  }
  
  const lengthOfEachWord = wordList.map(word => word.length)
  const index = lengthOfEachWord.indexOf(Math.max(...lengthOfEachWord))
  return {
    largestWord: wordList[index],
    largestWordIndex: index }
}

const s1 = "Buhari is a bad boy"
const s2 = "Wahala for who no sabi program"
const s3 = "Brooooo"

console.log(assignment(s1))
console.log(assignment(s2))
console.log(assignment(s3))
